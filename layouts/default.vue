<template>
  <div>
    <TheHeader @sidenavToggle="test"/>
    <TheSidenav
      :show="displaySidenav"
      @close="displaySidenav=false"/>
    <nuxt/>
  </div>
</template>

<style>
html {
  font-family: 'Nanum Gothic';
}
body {
  margin: 0;
}
</style>

<script>
import TheHeader from '@/components/Navigation/TheHeader'
import TheSidenav from '@/components/Navigation/TheSidenav'
export default {
  components: {
    TheHeader,
    TheSidenav
  },
  data: function() {
    return {
      displaySidenav: false
    }
  },
  methods: {
    test: function() {
      console.log(this.displaySidenav)
      this.displaySidenav = !this.displaySidenav
    }
  }
}
</script>
