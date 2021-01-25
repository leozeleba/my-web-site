<template>
    <div class="experience">
        <div class="experience-header">                        
            <img class="experience-logo" :src="experience.logo" :style="styleLogo(experience)" alt="">
            <p>{{experience.company}}</p> 
            <div>
                {{experience.role}}
            </div>
            <br>
            <div>
                {{period(experience)}}
            </div>
            <br><br>
            <a :href="experience.website" target="_blank" rel="noopener noreferrer">Visiter le site internet ></a>
        </div>
        <div class="experience-description">
            <p>{{experience.description}}</p>
        </div>
        <div class="map">
            <Map :map="experience.map"/>
        </div>
    </div>
</template>

<script>
import Map from './Map.vue'
export default {
    name: 'Exeperience',
    props: {
        experience: Object
    },
    methods: {

        period(experience){
            if(experience.end == ""){
                return experience.start;
            }
            return experience.start + "-" + experience.end;
        },
        styleLogo(experience){
            return "width: " + experience.logoWidth
        }
    },
    components:{
        Map
    }

}
</script>

<style lang="scss" scoped>

.experience{
    display: flex;
    margin: 0 auto;
}

.experience-description{
    width: 25em;
    text-align: justify;
    margin: 6em 2.5em;
;
}

.experience-logo{
    width: 150px;
    
}

.experience-header{
    margin: auto 2em

}

a{
    margin-top: 30px;
    color: black;
}

.map{
    margin: 4em 0em 4em 6em;

    width: 500px;
    border-radius: 5%;
    overflow: hidden;
}

</style>