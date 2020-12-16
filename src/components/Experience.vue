<template>
    <div class="experience">
        <div class="experience-header">                        
            <img class="experience-logo" :src="experience.logo" :style="styleLogo(experience)" alt="">
            <p>{{experience.company}}</p> <!-- if not on logo will be != '' -->
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
    </div>
</template>

<script>
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

}
</script>

<style lang="scss" scoped>

.experience{
    display: flex;
    margin: 0 auto;
}

.experience-description{
    width: 40em;
    text-align: justify;
    margin: auto 40px;
;
}

.experience-logo{
    width: 150px;
}

.experience-header{
    margin-left: 40px;
    padding-top: 20px;
    margin-bottom: 20px;
}

a{
    margin-top: 30px;
    color: black;
}

.link{
}
</style>