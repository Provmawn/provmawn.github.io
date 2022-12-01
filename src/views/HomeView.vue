<template>
  <div class="container">
    <BannerCard>Hello. I'm Amman. Programming is my passion.</BannerCard>
  </div>
</template>

<script>
// @ is an alias to /src
import BannerCard from '@/components/BannerCard.vue'

export default {
    name: 'HomeView',
    components: {
        BannerCard
    }
}
</script>

<style>
.home {
    color:white
}
</style>
