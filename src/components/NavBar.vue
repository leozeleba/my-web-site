<template>
    <div class="nav-bar">
        <div class="row" @click="navBarOpen = !navBarOpen">
            <font-awesome-icon v-if="navBarOpen" icon="angle-left" class="navbar-toggle toggle-open right"/>
            <font-awesome-icon v-else icon="angle-right" class="navbar-toggle center"/>
        </div>
        <div class="row">
            <ul class="categories">
                <li @click="scrollTo(category.link)" class="category" v-for="category in categories" :key="category.id">
                    <div class="col-icon">
                        <font-awesome-icon :icon="category.fa" class="category-icon"/>
                    </div>
                    <div v-show="navBarOpen">
                        <p class="category-name col">
                            {{ category.name }}
                        </p>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>


export default {
    
    name: 'NavBar',
    data(){
        return{
            navBarOpen: false,
            categories:[

                {
                    id: 1,
                    name: "Profil",
                    link: "profil",
                    fa: ["fas","user"]  
                },
                {
                    id: 3,
                    name: "Experiences",
                    link: "experiences",
                    fa: ["fas","user-tie"]  
                },
                {
                    id: 2,
                    name: "Formations",
                    link: "courses",
                    fa: ["fas","user-graduate"]  
                },
                {
                    id: 4,
                    name: "Compétences",
                    link: "skills",
                    fa: ["fas","laptop-code"]  
                },
                {
                    id: 5,
                    name: "Portfolio",
                    link: "portfolio",
                    fa: ["fas","coffee"]  
                },
                {
                    id: 6,
                    name: "Hobbies",
                    link: "hobbies",
                    fa: ["fas","guitar"]  
                },
                {
                    id: 7,
                    name: "Contact",
                    link: "contact",
                    fa: ["fas","at"]  
                }
                
            ]
        }
    },
    methods:{
        scrollTo(id){
            document.getElementById(id).scrollIntoView();
        }
    }

}
</script>

<style lang="scss" scoped>

.row{
    display: flex;
    flex-direction: row;
}

.right{
    position: 0 20px;
    float: right;   
}

.center{
    padding: 0;
    position: 0 auto;
    width: 100%
}

.navbar-toggle{ 
    margin-top: 5px;
    font-size: 30px;
    cursor: pointer;
    color: #dfdfdf;
}

.toggle-open{
    margin: 5px 20px 0px 0px;
    padding-left: 9em;
}

.nav-bar{
    background-color: #1c1c1c;
    position: fixed;
    width: min-content;
}


.categories{
    display: inline-block;
    margin:0;
    margin-left: 40px
}

.category{
    white-space: nowrap;
    display: flex;
    padding-right: 30px;
    padding: 15px 30px 25px 0;
    cursor: pointer;
    color:#b7b7b7;
}


.category-name{
    text-transform: uppercase;
    font-weight: bold;
    margin: 0px;
    font-size: 25px;
    height:25px
}

.category:hover{
    color: white
    ;
}

.navbar-toggle:hover{
    color: white
    ;
}

.category-icon{
    margin: 0;
}


.col-icon{
    width: 0px;
    margin-right: 40px;
    height:25px;
    font-size: 25px;
}

</style>