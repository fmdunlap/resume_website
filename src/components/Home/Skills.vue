<template>
  <div class="container flex-container"
        data-aos="fade-right" 
        data-aos-anchor-placement="top-bottom"
        data-aos-duration="1000">
    <div id="languages">
      <h1>LANGUAGES</h1>
      <ul>
        <li v-for="lang in languages" v-bind:key="languages.indexOf(lang)">
          {{lang}}
        </li>
      </ul>
    </div>
    <div id="skills">
      <h1>SKILLS</h1>
      <ul>
        <li v-for="skill in skills" v-bind:key="skills.indexOf(skill)">
          {{skill}}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      skills: [
        "Android Development",
        "Web Development",
        "CAD",
        "Leadership",
        "Communication",
        "Cooking"
      ],
      languages: [
        "Java",
        "Python",
        "JavaScript",
        "C++",
        "Kotlin"
      ]
    }
  }
}
</script>

<style>
.flex-container{
  display: flex;
  width: 50%;
  padding: 30px;
  flex-wrap:wrap;
  max-width: 1300px;
}

.flex-container li{
  list-style: none;
}

#languages{
  flex: 1;
}

#skills{
  flex: 1;
}

</style>
