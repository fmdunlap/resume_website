<template>
    <header id="header">
        <div id="nav">
            <div id="page-links">
                <ul>
                    <li v-bind:class="{ selected : this.$route.path === '/'}" ><router-link to="/">HOME</router-link></li>
                    <!-- <li v-bind:class="{ selected : this.$route.path === '/blog'}"><router-link to="/blog">BLOG</router-link></li> -->
                    <li v-bind:class="{ selected : this.$route.path === '/portfolio'}"><router-link to="/portfolio">PORTFOLIO</router-link></li>
                    <li v-bind:class="{ selected : this.$route.path === '/contact'}"><router-link to="/contact">CONTACT</router-link></li>
                </ul>
            </div>
            <div id="social">
                <ul>
                    <li><a href="https://www.linkedin.com/in/forrest-dunlap/"><img src="../../assets/social/linkedin.png"></a></li>
                    <li><a href="https://github.com/fmdunlap"><img src="../../assets/social/github.png"></a></li>
                    <li><a href="https://open.spotify.com/user/fmdunlap"><img src="../../assets/social/spotify.png"></a></li>
                    <li><a href="https://www.instagram.com/the_forrest_fire/"><img src="../../assets/social/insta.png"></a></li>
                    <li><a href="https://www.facebook.com/FmdunlapIV"><img src="../../assets/social/facebook.png"></a></li>
                </ul>
            </div>
        </div>
    </header>
</template>

<script>
import chroma from 'chroma-js'

var transparent = chroma("#2A2A2A00").hex();
var opaque = chroma("#2A2A2ACC").hex();
var header_scale = chroma.scale([transparent, opaque])
header_scale.mode('lrgb');
header_scale.cache(true);

export default {
    name: 'Header',
    methods: {
        handleScroll(event){
            let head = document.getElementById("header");
            let hero = document.getElementById("hero-container");
            let height = hero.scrollHeight - (scrollY + head.scrollHeight);
            let trigger = 4*head.scrollHeight;

            if(height > trigger){
                head.style.background = chroma(transparent).hex();
            } else if(height <= trigger && height >= 0){
                let p = height / (trigger);
                head.style.background = chroma(header_scale(1 - p))
                console.log(p);
            } else {
                head.style.background = chroma(opaque).hex();
            }
        }
    },
    created(){
        window.addEventListener('scroll', this.handleScroll);
    },
    destroyed(){
        window.removeEventListener('scroll', this.handleScroll);
    }
}
</script>

<style>

header {
    z-index: 999;
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
}

a {
    color: white;
    text-decoration: none;
}

#nav ul {
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;
    margin: 20px 0;
}

#nav #page-links{
    float: left;
    margin-left: 7%;
}

#nav #page-links li{
    margin-right: 40px;
    padding: 4px;
}

#nav #social{
    float: right;
    margin-right: 7%;
}

#nav #social li {
    margin-left: 40px;
}

.selected {
    background: #FFF;
    border-radius: 5px;
}

.selected a {
    color: #0D2E0C;
}

@media screen and (max-width: 865px){
    #social{
        display: none;
    }
}

</style>
