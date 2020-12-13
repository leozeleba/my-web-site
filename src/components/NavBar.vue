<template>
    <div class="nav-bar">
        <h1>NAVBAR</h1>
        <ul>
            <li class="category" v-for="category in categories" :key="category.id">
                <h2 class="category-name">{{ category.name }}</h2>
            </li>
        </ul>
    </div>
</template>

<script>


export default {
    name: 'NavBar',
    data(){
        return{
            categories:[

                {
                    id: 1,
                    name: "Profile",
                    link: "/profile",
                    svg: ""  
                },
                {
                    id: 2,
                    name: "Formations",
                    link: "/courses",
                    svg: ""  
                },
                {
                    id: 3,
                    name: "Experiences",
                    link: "/experiences",
                    svg: ""  
                },
                {
                    id: 4,
                    name: "Compétences",
                    link: "/skills",
                    svg: ""  
                },
                {
                    id: 5,
                    name: "Portfolio",
                    link: "/portfolio",
                    svg: ""  
                },
                {
                    id: 6,
                    name: "Hobbies",
                    link: "/hobbies",
                    svg: ""  
                },
                {
                    id: 7,
                    name: "Contact",
                    link: "/contact",
                    svg: ""  
                }
                
            ]
        }
    }

}
</script>

<style lang="scss" scoped>

    .nav-bar{
        background-color: rgb(255, 255, 255);
        border-right: grey solid 2px;
        width: 23%;
    }

    .nav-bar > ul{
        list-style-type: none;
        
    }

    .category{
        margin: 20px 0px;
    }

    .category-name{
        text-transform: uppercase;
    }


</style>