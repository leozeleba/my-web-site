<template>
    <div class="course">
        <div class="course-header">                        
            <img class="course-logo" :src="course.logo" :style="styleLogo(course)" alt="">
            <p>{{course.company}}</p> <!-- if not on logo will be != '' -->
            <br>
            <div>
                {{period(course)}}
            </div>
            <br><br>
        </div>
        <div class="course-description">
            <div>
                {{course.name}}
            </div> 
            <p>{{course.description}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Course',
    props: {
        course: Object
    },
    methods: {

        period(course){
            if(course.end == ""){
                return course.start;
            }
            return course.start + "-" + course.end;
        },
        styleLogo(course){
            return "width: " + course.logoWidth
        }
    },

}
</script>

<style lang="scss" scoped>

.course{
    display: flex;
    margin: 0 auto;
}

.course-description{
    width: 40em;
    text-align: justify;
    margin: auto 40px;
;
}

.course-logo{
    width: 150px;
}

.course-header{
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