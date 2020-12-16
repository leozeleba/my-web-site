<template>
  <div class="main">
    
    <div class="nav-bar">
      <NavBar class="nav-bar-element"/>
    </div>
    <div>
      <Profil class="profil-element" />
      <Experiences/>
      <Courses/>
    </div>
    
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from '@/components/NavBar.vue'
import Profil from '@/components/Profil.vue'
import Experiences from '@/components/Experiences'
import Courses from '@/components/Courses'

export default {
  name: 'Home',
  components: {
    NavBar,
    Profil,
    Experiences,
    Courses
  }
}
</script>

<style lang="scss" scoped>

.main{
  display: flex;
}

.nav-bar{
  z-index: 10;
}
.nav-bar-element{
  height:100%
}

.profil-element{
  height: 400px;
  box-shadow: 6px 5px 5px #737373;

}
</style>
