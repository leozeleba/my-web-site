<template>
        <div class="comp">
            <p class="skill-label">{{skill.label}}</p>
            <div v-if="skill.fa != null">
                <font-awesome-icon  :icon="skill.fa" :size="skill.iconSize" class="skill-icon" />
            </div>
            <div v-else-if="skill.img != ''">
                <img  :src="skill.img" :style="skill.style"/>
            </div>
        </div>
</template>

<script>
export default {
    name:'Skill',
    props:{
        skill: Object,
    },
    data(){
        return{    
        }
    },
    mounted(){
    }

}

</script>

<style lang="scss" scoped>

.comp{
    border-radius: 50%;
    background: #bbb;
    box-shadow: 6px 5px 5px #737373;
    text-align: center;
    margin: 5px 3px;
}

.skill-icon{
    padding-bottom:40px
}

.skill-label{
    padding-top: 20px;
    font-size: 25px;
}

</style>