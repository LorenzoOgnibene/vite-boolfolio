<script>
    import axios from 'axios';
    export default{

        data(){
            return {
                projects: [],
            }
        },
        methods: {
            getApi(){
                axios.get('http://127.0.0.1:8000/api/projects')
                .then((response) => {
                    console.log(response.data.results )
                    this.projects = response.data.results
                    console.log(this.card)
                })  
            }
        },

        mounted(){
            this.getApi();
        }
    }
    
</script>

    <template>
        <div class="container">
            <div class="row g-4">
                <div class="col-4 d-flex d-wrap" v-for="project in projects">
                    <div class="card">
                        <div class="card-header text-center">
                            <span class="badge text-bg-info me-2" v-for="tecnology in project.tecnologys">{{ tecnology.name }}</span>
                            <h5>{{ project.type.name }}</h5>
                        </div>
                        <img :src="project.image" class="card-img-top" alt="">
                        <div class="card-body">
                            <h5 class="card-title fw-bold">{{project.title}}</h5>
                            <p class="card-text">{{project.description.substr(0,200)}}</p>
                            <h6 class="card-subtitle text-muted mb-3">{{ project.creation_date }}</h6>
                            <div class="d-flex"> 
                                <a :href="project.id" class="btn btn-primary">Go somewhere</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </template>

<style lang="scss">

    

</style>