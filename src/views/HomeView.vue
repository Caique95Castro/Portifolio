<template>
  <div class="home">
    <HomeTemplate/>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeTemplate from '@/components/HomeTemplate.vue'

export default {
  name: 'HomeView',
  components: {
    HomeTemplate
  }
}
</script>
