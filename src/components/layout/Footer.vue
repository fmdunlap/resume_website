<template>
    <footer id="footer">
        <div id="social">
            <ul>
                <li><a href="https://www.linkedin.com/in/forrest-dunlap/"><img src="../../assets/social/linkedin.png"></a></li>
                <li><a href="https://github.com/fmdunlap"><img src="../../assets/social/github.png"></a></li>
                <li><a href="https://open.spotify.com/user/fmdunlap"><img src="../../assets/social/spotify.png"></a></li>
                <li><a href="https://www.instagram.com/the_forrest_fire/"><img src="../../assets/social/insta.png"></a></li>
                <li><a href="https://www.facebook.com/FmdunlapIV"><img src="../../assets/social/facebook.png"></a></li>
            </ul>
        </div>
        <br/>
        <p>Built by Forrest Dunlap & Designed by Michelle Sacks, &copy; 2019</p>
    </footer>
</template>

<script>
export default {

}
</script>

<style>
#footer{
    background: #2A2A2A;
    height: max-content;
    padding: 20px 0px;
}

#footer p{
    color: white;
}

#footer #social ul{
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;
    float: none;
    justify-content: center;
}

#social li {
    margin: 0px 20px;
}
</style>