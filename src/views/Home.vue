<template>
  <div>
        
    <body class="main">
      <div class="nav-bar">
        <NavBar class="nav-bar-element"/>
      </div>
      <div class="content">
        <div class="banner profil-element">
          <h1 class="title">Qui est Léo Bories ?</h1>
        </div>
        <Profil id="profil" class="profil-element" />
        <br>
        <Experiences id="experiences"/>
        <br>
        <Courses id="courses"/>
        <br>
        <Skills id="skills" class="skills-element"/>
        <br>
        <Portfolio id="portfolio" class="portfolio-element" />
      </div>
    </body>
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from '@/components/NavBar.vue'
import Profil from '@/components/Profil.vue'
import Experiences from '@/components/Experiences.vue'
import Courses from '@/components/Courses.vue'
import Skills from '@/components/Skills.vue'
import Portfolio from '@/components/Portfolio.vue'

export default {
  name: 'Home',
  components: {
    NavBar,
    Profil,
    Experiences,
    Courses,
    Skills,
    Portfolio
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
  
  box-shadow: 6px 5px 5px #737373;
}

.banner{
  height: 100px;
  background-color: #737373;
  margin-bottom: 40px;

}
.content{
  padding-left:130px;
}

.title{
  text-align: center;
  padding-top: 0.8em;
}

.portfolio-element{
  margin-top: 5em;
}

</style>
