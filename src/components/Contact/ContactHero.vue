<template>
    <div id="hero-container">
        <h1>CONTACT ME</h1>
        <form id="contact-form">
            <input type="text" name="name" placeholder="NAME" v-model="name">
            <input type="text" name="email" placeholder="EMAIL" v-model="email">
            <input type="text" name="subject" placeholder="SUBJECT" v-model="subject">
            <textarea name="message" placeholder="MESSAGE" v-model.trim="message"/>
            <input type="submit" value="SEND" v-on:click.prevent="processSend"/>
        </form>
    </div>
</template>

<script>
import axios from 'axios'

const client = axios.create({
    baseURL: 'http://localhost:3000/api/',
    json: true
})

export default {
    name: "contact_hero",
    data: function(){
        return{
            name: '',
            email: '',
            subject: '',
            message: ''
        }
    },
    methods: {
        processSend: function(){
            client({
                method: 'post',
                url: '/message',
                data: {
                    name: this.$data.name,
                    email: this.$data.email,
                    subject: this.$data.subject,
                    message: this.$data.message
                }
            })
        }
    }
}
</script>

<style>
#hero-container{
    display: flex;
    margin-left: 0;
    height: 100vh;
    background-image: url("../../assets/home/hero/hero_2560.jpeg");
    background-position: left center;
    background-size: cover;
    background-color: #777;
    background-blend-mode: multiply;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

#hero-container h1{
    color: white;
}

#hero-container form{
    display: flex;
    flex-direction: column;
    width: 55%;
}

#hero-container form *{
    flex: 1;
    margin-bottom: 12px;
    line-height: 2.25em;
    border-radius: 5px;
    padding-left: 5px;
    border: none;
    background: #F3F3F3;
    font-family: Muli;
}

#hero-container form textarea{
    flex: 3;
    padding-top: 10px;
    padding-bottom: 10px;
    line-height: 1em;
    height: 10em;
    resize: none;
}

#hero-container form input[type=submit]{
    margin-left: 80%;
    margin-top: 10%;
    font-family: Muli;
    font-size: 18px;
    background: #414141;
    color: white;
    border: solid #FFF 1px;
    cursor: pointer;
}

::-webkit-input-placeholder { /* Chrome/Opera/Safari */
    color: #0000009D;
    font-family: Muli;
}
::-moz-placeholder { /* Firefox 19+ */
    color: #0000009D;
    font-family: Muli;
}
:-ms-input-placeholder { /* IE 10+ */
    color: #0000009D;
    font-family: Muli;
}
:-moz-placeholder { /* Firefox 18- */
    color: #0000009D;
    font-family: Muli;
}

@media screen and (min-width: 1200px){
    #hero-container form{
        width: 40em;
    }
}

@media screen and (max-width: 520px){
    
    #hero-container form{
        width: 80%;
    }

    #hero-container h1{
        padding-bottom: 15%;
        font-weight: bold;
        font-size: 2em;
    }

}


</style>
