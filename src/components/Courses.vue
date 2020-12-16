<template>
    <div class="comp">
        <ul class="couse-list">
            <li class="course-element" v-for="course in coursesList" :key="course.id">
                <Course :course="course"/>
            </li>
        </ul>
    </div>
</template>

<script>

import logo_iut_limoges from "@/assets/logo_iut_limoges.png"
import logo_iut_vannes from "@/assets/logo_iut_vannes.png"
import logo_42 from "@/assets/logo_42.png"
import Course from './Course.vue'

export default {
    
    
    name: 'Courses',
    components:{
        Course

    },
    data(){
        return{
            coursesList: [
                {
                    id: 1,
                    name: "Licence professionnelle de développement d’application web à l’université de Limoges",
                    start: "09/2019",
                    end: "06/2020",
                    description: "Cette formation m’a permis de continuer l’apprentissage et, de consolider mes compétences dans le métier de développeur informatique.",
                    logo: logo_iut_limoges,
                    logoWidth: "150px",
                },
                {
                    id: 2,
                    name: "Diplôme universitaire d’Informatique à l’université de Vannes",
                    start: "09/2017",
                    end: "06/2019",
                    description: "Lors de ces deux années de formation universitaire j’ai découvert le développement informatique, et le monde de l’entreprise lors de ma deuxième année en apprentissage.",
                    logo: logo_iut_vannes,
                    logoWidth: "150px",
                },
                {
                    id: 3,
                    name: "",
                    role: "Développeur logiciel",
                    start: "03/07/2017",
                    end: "30/07/2017",
                    description: "Lors de ces deux années de formation universitaire j’ai découvert le développement informatique, et le monde de l’entreprise lors de ma deuxième année en apprentissage.",
                    logo: logo_42,
                    logoWidth: "100px",
                }
            ]
        }
    }

}
</script>

<style lang="scss" scoped>

.comp{
    background-color: white;
}

.couse-list{
}

.course-element{
    display: flex;
    background-color: #bbb;
    box-shadow: 6px 5px 5px #737373;
    margin: 30px auto;
}

</style>