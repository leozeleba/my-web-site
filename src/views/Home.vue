<template>
  <div class="main">
    
    <div class="nav-bar">
      <NavBar class="nav-bar-element"/>
    </div>
    <div>
      <Profil class="profil-element" />
      <Courses/>
    </div>
    
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from '@/components/NavBar.vue'
import Profil from '@/components/Profil.vue'
import Courses from '@/components/Courses'

export default {
  name: 'Home',
  components: {
    NavBar,
    Profil,
    Courses
  }
}
</script>

<style lang="scss" scoped>

.main{
  display: flex;
}

.nav-bar{
}
.nav-bar-element{
  height:100%
}

.profil-element{
}
</style>
