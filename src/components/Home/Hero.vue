<template>
    <div id="hero-container">
        <div id="hero-text">
            <h3>I AM</h3>
            <h1>FORREST DUNLAP</h1>
            <h3><img src="../../assets/home/hero/line.png" class="l">AND I AM A<img src="../../assets/home/hero/line.png" class="r"></h3>
            <h2>SOFTWARE ENGINEER</h2>
        </div>
    </div>
</template>

<script>
export default {
    name: "home_hero"
}
</script>

<style>
#hero-container{
    display: flex;
    margin-left: 0;
    height: 100vh;
    background-image: url("../../assets/home/hero/hero_background_3-min.jpg");
    background-position: left center;
    background-size: cover;
    background-color: #777;
    background-blend-mode: multiply;
    align-items: center;
    justify-content: center;
}

#hero-text{
    color: white;
    font-size: calc(1em + 1vw);
}

#hero-text h1{
    font-weight: 300;
    font-size: calc(1.7em + 1vw);
    letter-spacing: .02em;
    line-height: 1.5em;
}

#hero-text h3{
    width: 100%;
    font-weight: 300;
    font-size: calc(.3em + 1vw);
}

#hero-text h2{
    font-family: 'Permanent Marker', cursive;
    font-size: calc(1em + 1vw);
    line-height: 5rem;
}

#hero-text img{
    vertical-align: middle;
    height: 1px;
    margin: 0px 1.5%; 
    width: 4em;
}

/* @media screen and (min-width: 1200px){
    #hero-text{
        padding-top: 14%;
        padding-bottom: 14%;
    }

    #hero-text h2{
        line-height: 1.25em;
    }
}

@media screen and (max-width: 520px){
    #hero-text{
        padding-top: 55px;
        padding-bottom: 16%;
    }

    #hero-text h2{
        line-height: 1.25em;
    }
} */


</style>
