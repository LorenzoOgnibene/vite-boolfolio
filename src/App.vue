<script>
    import ProjectCard from './components/ProjectCard.vue';
    import SingleCard from './components/SingleCard.vue';
    export default {
       name: 'App', 

        components : {
            ProjectCard,
            SingleCard,
        },

        data() {
            return {
                
            }
        },
    }

</script>

<template>
    <!-- <ProjectCard /> -->
    <SingleCard/>
</template>

<style lang="scss">
 @use 'bootstrap/scss/bootstrap' as *;
</style>
