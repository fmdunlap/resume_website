<template>
    <div id="about-me" class="container" 
        data-aos="fade-right" 
        data-aos-anchor-placement="center-bottom"
        data-aos-duration="1000"
        >
        <h1>ABOUT ME</h1>
        <div class="content">
            <img id="profile" src="../../assets/home/aboutme/img_me.png"/>
            <ul>
                <li>I lived in <a>Austin, TX.</a></li>
                <li>I moved to Los Angeles, CA for <a>school.</a></li>
                <li>I met a <a href="https://michellesacks.com/">girl</a> at USC.</li>
                <li>I moved to Seattle, WA for <a>6 months.</a></li>
                <li>I am moving to <a>Mountain View, CA</a> in June.</li>
                <li>I (try to) write <a>code</a> every day.</li>
                <li>I last read <a>"Superintelligence"</a> by Nick Bostrom.</li>
                <li>I play <a>video games</a> in my spare time.</li>
                <li>I really love <a>cooking</a> as a hobby.</li>
                <li>I love <a>dogs.</a> But cats are okay, too.</li>
            </ul>
        </div>
        <hr/>
    </div>
</template>

<script>
export default {
    name: "home_about"
}
</script>

<style>

.container h1{
    margin: 2%;
    font-weight: 300;
    font-size: 45px;
}

.content{
    display: flex;
    margin: auto;
    align-content: center;
    width: max-content;
}

.content ul {
    margin-left: 1em;
}

.content li{
    color: black;
    list-style: none;
    text-align: left;
    line-height: 2em;
    font-size: 1.2rem;
}

.content a{
    color: #004E14;
    font-weight: bold;
}

.content a:hover{
    text-decoration: none;
    cursor: pointer;
}

img#profile{
    height:auto;
    align-self: center;
    float: left;
    image-rendering: optimizeQuality;
    margin: 0;
    border-radius: 5px;
}

@media screen and (max-width: 815px){
    .content{
        flex-direction: column;
        font-size: 30px;
    }
    img#profile{
        height:420px;
        float: none;
    }
    .content ul{
        margin-top: 10px;
    }
    .content li{
        color: black;
        list-style: none;
        text-align: center;
        line-height: 2em;
        font-size: 1.2rem;
    }
}

@media screen and (max-width: 550px){
    img#profile{
        height: 360px;
    }
    .content li{
        font-size: .5em;
    }
}



</style>
