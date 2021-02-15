<template>
    <div class="comp">
        <ul class="skill-list">
            <li v-for="skill in listSkills" :key="skill.id">
                <Skill class="skill-element" :skill="skill"/>
            </li>
        </ul>
    </div>
</template>

<script>
import Skill from './Skill'
import windevImage from "@/assets/windev-logo.png"
import mysqlImage from "@/assets/mysql-logo.png"
import leafletImage from "@/assets/leaflet-logo.png"
import htImage from "@/assets/handsontable_logo.png"
import mdbImage from "@/assets/mongodb.png"

export default {
    name:'Skills',
    components:{
        Skill
    },
    data(){
        return{
            listSkills:[
                {
                    id: 1,
                    label: "Linux",
                    fa: ["fab","linux"],
                    iconSize: "5x",
                    img: "",
                    style: ""
                },
                {
                    id: 2,
                    label: "POO",
                    fa: ["fas","cubes"],
                    iconSize: "5x",
                    img: "",
                    style: ""
                },
                {
                    id: 3,
                    label: "Java",
                    fa: ["fab","java"],
                    iconSize: "5x",
                    img: "",
                    style: ""
                },
                {
                    id: 4,
                    label: "Windev",
                    fa: null,
                    iconSize: "1x",
                    img: windevImage,
                    style: "width: 96px; margin-bottom: 20px;"
                },
                {
                    id: 5,
                    label: "Symfony",
                    fa: ["fab","symfony"],
                    iconSize: "5x",
                    img: "",
                    style: ""
                },
                {
                    id: 6,
                    label: "Vue",
                    fa: ["fab","vuejs"],
                    iconSize: "5x",
                    img: "",
                    style: ""
                },{
                    id: 7,
                    label: "Angular",
                    fa: ["fab","angular"],
                    iconSize: "5x",
                    img: "",
                    style: ""
                },
                {
                    id: 8,
                    label: "Javascript",
                    fa: ["fab","js"],
                    iconSize: "5x",
                    img: "",
                    style: ""
                },
                {
                    id: 9,
                    label: "MySQL",
                    fa: null,
                    iconSize: "1x",
                    img: mysqlImage,
                    style: "width: 95px;margin-bottom: 21px;"
                },
                {
                    id: 10,
                    label: "HTML",
                    fa: ["fab","html5"],
                    iconSize: "5x",
                    img: "",
                    style: ""
                },
                {
                    id: 11,
                    label: "CSS",
                    fa: ["fab","css3-alt"],
                    iconSize: "5x",
                    img: "",
                    style: ""
                },
                {
                    id: 12,
                    label: "Git",
                    fa: ["fas","code-branch"],
                    iconSize: "5x",
                    img: "",
                    style: ""
                },
                {
                    id: 13,
                    label: "Leaflet",
                    fa: null,
                    iconSize: "1x",
                    img: leafletImage,
                    style: "padding-bottom: 20px;margin-top: -46px;"
                },
                {
                    id: 14,
                    label: "Handsontable",
                    fa: null,
                    iconSize: "1x",
                    img: htImage,
                    style: "padding-bottom: 20px; width:100px"
                },
                {
                    id: 15,
                    label: "MongoDB",
                    fa: null,
                    iconSize: "1x",
                    img: mdbImage,
                    style: "padding-bottom: 20px; width:100px"
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

.skill-element{
    width:200px;
    box-shadow: 6px 5px 5px #737373;
    margin: 10px 10px;
}

.skill-list{
    display:flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
}


</style>