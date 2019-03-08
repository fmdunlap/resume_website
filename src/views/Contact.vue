<template>
  <div class="contact">
    <Hero/>
  </div>
</template>

<script>
import Hero from '../components/Contact/ContactHero.vue'

export default {
  name: 'contact',
  components: {
    Hero
  }, 
  created(){
    document.title = "Forrest Dunlap | Contact" 
  }
}
</script>

