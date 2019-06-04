<style>
#education{
  display: flex;
  flex-direction: column;
}

.mobile{
  display: none;
}

.desktop{
  display: block;
}

h1{
  margin: 2% 0;
  font-size: 45px;
  font-weight: 300;
}

.education-entry{
    display:flex;
    flex-direction: column;
    width: 50%;
    min-width: 700px;
    margin: auto;
}

.education-entry h1{
    font-size: 1em;
    font-weight: bold;
    text-align: left;
    width: 100%;
    margin: 12px auto;
    line-height: 0;
}

.education-entry h2{
    font-size: 1em;
    font-weight: 400;
    text-align: left;
    width: 100%;
    margin: 0 auto;
    line-height: 1em;
}

.body {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
}

.education-entry .body img{
    margin-top: 15px;
    margin-left: 10px;
    width: 10px;
    max-width: 60px;
    flex-basis: auto;
    flex: 1;
    align-self: flex-start;
}

.education-body-text{
  margin: 20px;
  list-style: none;
}

.education-body-text h1{
  display: inline;
  font-weight: bold;
}

.right{
  float: right;
}

@media screen and (max-width: 768px){
  .mobile{
    display: block;
  }

  .desktop{
    display: none;
  }

  .education-entry{
    align-self: center;
  }

  .education-entry h1{
    font-size: 14px;
    line-height: 1em;
  }

  .education-entry h2{
    font-size: 14px;
    line-height: 1em;
  }

  .education-body-text{
    font-size: 12px;
  }
}

</style>


<template>
    <div class="education container" 
        data-aos="fade-right" 
        data-aos-anchor-placement="center-bottom"
        data-aos-duration="1000"
        >
        <h1>EDUCATION</h1>
        <div class="education-entry">
            <div class="desktop"><h1>B.S. Computer Engineering & Computer Science <span class="right">August 2014 - May 2019</span></h1></div>
            <div class="desktop"><h2>University of Southern California <span class="right">Los Angeles, CA</span></h2></div>
            <div class="mobile"><h1>B.S. Computer Engineering & Computer Science</h1></div>
            <div class="mobile"><h2>University of Southern California (2014 - 2019)</h2></div>
            <div class="body">
                <img class="badge"  :src="require('../../assets/home/resume/usc_badge.png')">
                <ul class="education-body-text">
                  <li><h1>Sigma Eta Pi</h1> - New Member Educator</li>
                  <li><h1>HackSC</h1> - Director of Special Projects</li>
                </ul>
            </div>
        </div>
        <hr/>
    </div>
</template>

<script>
export default {
    
}
</script>