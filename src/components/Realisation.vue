<template>
        <div class="comp">
            <p class="skill-label">{{realisation.label}}</p>
            <div v-for="(otherText,index) in realisation.otherText" :key="index" :style="realisation.style">
                <p class="skill-otherText">{{otherText}}</p>
            </div>
            <br/>
            <div>

            <img :src="realisation.img" :style="realisation.imgStyle"/>
            </div>
            <div v-if="realisation.template != null">
                <span v-html="realisation.template" class='additionnal-template'></span>
            </div>

        </div>
</template>


<script>
export default {
    name:'Realisation',
    components:{
    },
    props:{
        realisation: Object,
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
    display: inherit;
}
.skill-label{
    margin-left: 1em;
    margin-top: 0.5em;
    margin-right: 1em;
    
}
.skill-otherText{
    margin-left: 2em;
    margin-top: 1em;
    margin-right: 2em;
    text-align: justify;    
}

.additionnal-template{
    width: 200px
}



</style>