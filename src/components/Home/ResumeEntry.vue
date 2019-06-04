<template>
    <div class="resume-entry">
        <h1>{{job.title}}, <span class="location">{{job.location}}</span><br id="mobile-break"/><span class="date">{{job.date}}</span></h1>
        <div class="body">
            <img class="badge"  :src="require('../../assets/home/resume/'+job.badge+'_badge.png')">
            <ul class="resume-body-text">
                <li v-for="bullet in job.body" v-bind:key="job.body.indexOf(bullet)">
                    {{bullet}}
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: "home_resume_entry",
    props: [
        "job"
    ]
}

</script>

<style>
.resume-entry{
    display:flex;
    flex-direction: column;
    width: 50%;
    margin: auto;
    min-width: 700px;
    flex-wrap:wrap;
}

.resume-entry h1{
    font-size: 1em;
    font-weight: bold;
    text-align: left;
    width: 100%;
    margin: 12px auto;
}
.resume-entry h1 .location{
    font-weight: 300;
}

.resume-entry #mobile-break {
    display:none;
}

.resume-entry h1 .date{
    float: right;
}

.resume-entry .body{
    display: flex;
    align-content: center;
    justify-content: flex-start;
}

.resume-entry .body img{
    margin-top: 10px;
    margin-left: 10px;
    width: 10px;
    max-width: 60px;
    min-width: 50px;
    flex-basis: auto;
    flex: 1;
    align-self: flex-start;
}

.resume-body-text{
    flex: 10;
    margin-top: 10px;
    margin-bottom: 10px;
    margin-left: 20px;
    font-weight: 400;
    font-size: 16px;
    line-height: 1.5em;
}

.resume-body-text li{
    margin-bottom: 10px;
    word-wrap: normal;
    text-align: left;
}

.resume-body-text > li:first-child{
    list-style: none;
}

.resume-body-text > li:not(:first-child){
    margin-left: 20px;
}

@media screen and (max-width: 768px){
    .resume-entry #mobile-break{
        display:block;
    }

    .resume-entry h1{
        font-size: 14px;
        width:100%;
        align-self: left;
        overflow-wrap: unset;
    }

    .resume-entry h1 .date{
        float: none;
    }

    .resume-body-text{
        flex: 10;
        margin-top: 10px;
        margin-bottom: 10px;
        margin-left: 20px;
        font-weight: 400;
        font-size: 13px;
        line-height: 1.5em;
    }

    .resume-entry{
        width: 100%;
        min-width: 0px;
    }
}

@media screen and (max-width: 550px){
    
    .resume-entry h1{
        font-size: 12px;
    }
    .resume-body-text{
        font-size: 11px;
    }
}

</style>
