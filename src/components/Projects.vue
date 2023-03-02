<script>
    import axsion from 'axios';
    export default{

        data(){
            return {
                
            }
        },
        methods: {
            getApi(){
                axsion.get('http://127.0.0.1:8000/api/projects')
                .then((response) =>
                    console.log(response.data)
                )
            }
        },

        mounted(){
            this.getApi();
        }
    }
    
</script>

    <template lang="">

    </template>

<style lang="scss">

    

</style>