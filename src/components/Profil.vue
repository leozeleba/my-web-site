<template>
    <div class="profil">
        <div class="col-img">
            <a href="/about">about</a>
            <img :src="mainImg" alt="" class="main-image">
        </div>
        <div class="col-text">
            <p class="main-text">{{mainText}}</p>
        </div>
    </div>
</template>

<script>
import mainImage from "@/assets/Photo_de_profil.jpg"

export default {
    
    name: 'Profil',
    data(){
        return{
            mainText: "Après deux années d’apprentissage dans deux entreprises différentes, j’ai découvert le métier de développeur en informatique. Ce métier passionnant est pour moi gratifiant car, il me permet de réaliser des projets qui répondent à un ou plusieurs besoins, dans un domaine que je maitrise. Je souhaite pour mon prochain emploi être amené à découvrir de nouvelles technologies, échanger avec mes futures collègues sur des solutions à un problème complexe et, pouvoir proposer de nouvelles idées. Je suis quelqu’un de rigoureux, de créatif et surtout, quelqu’un de persévérant.",
            mainImg: mainImage
        }
    }

}
</script>

<style lang="scss" scoped>

.row{
    display: block ruby;
    flex-direction: row;
}

.right{
    position: 0 20px;
    float: right;   
}


.profil{
    display: flex;
    align-items: center;
    background-color: #bbb;
}

.main-image{
    width: 200px;
    border-radius: 50% ;
    border: solid 2px black;
    margin: 100px 40px
}

.main-text{
    text-align: justify;
    margin: 0 40px 0 0;

}

.col-img{
    height:100%;
}

.col-text{
    width: 70%;
}

</style>