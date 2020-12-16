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

import logo_ganacos from "@/assets/logo_ganacos.png"
import logo_progidys from "@/assets/logo_progidys.png"
import logo_etib from "@/assets/logo_etib.png"
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
                    company: "",
                    role: "Développeur full-stack",
                    start: "14/10/1999",
                    end: "",
                    description: "Ganacos est une nouvelle entreprise qui développe une application web pour la planification d’une entreprise. Ce fut pour moi une expérience gratifiante de part, les responsabilités que l’on m’avait confiées et, le challenge technique que représente l’application Ganacos.",
                    logo: logo_ganacos,
                    logoWidth: "150px",
                    website: "https://ganacos.com/"
                },
                {
                    id: 2,
                    company: "",
                    role: "Chef de projet junior",
                    start: "09/2019",
                    end: "06/2020",
                    description: "Progidys est une PME dans l’édition d’ERP. Étant donné le petit nombre d’employés, j’ai dû faire preuve d’une grande autonomie et j’ai aimé avoir l’opportunité de toujours proposer de nouvelles idées, façon de développer, pour répondre au mieux au besoin d’un client et améliorer l’expérience utilisateur.",
                    logo: logo_progidys,
                    logoWidth: "150px",
                    website: "https://www.progidys.fr/"
                },
                {
                    id: 3,
                    company: "",
                    role: "Développeur logiciel",
                    start: "12/2018",
                    end: "08/2019",
                    description: "L’entreprise ETIB c’est spécialisé dans l’édition de logiciels à destination des professionnels du transport et du transport médical (taxi, ambulance, taxis conventionnés…). J’ai appris à réaliser un projet de façon méthodique pour toujours trouver la meilleure façon de résoudre un ou plusieurs problèmes.",
                    logo: logo_etib,
                    logoWidth: "100px",
                    website: "http://www.etib.fr/FR/"
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