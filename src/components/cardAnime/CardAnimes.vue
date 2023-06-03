<script>
    import axios from'axios'
    import { BCollapse , BButton,BPagination} from 'bootstrap-vue';

    export default{
        name : 'CardAnimes',
        comments:{
            BButton,
            BCollapse,
            BPagination
        },
        data() {
            return {
                // secretKey:,
                rows: 10,
                perPage: 1,
                currentPage: 1,
                anime_res_mal: {},
                
            };
        },
        mounted(){
            this.get_animes_mal(1)
        },
        methods:{
            get_animes_mal(page){

                
                let offset = (page-1)*10
                let url = `http://localhost:8080/v2/anime/ranking?limit=10&offset=${offset}&ranking_type=bypopularity&fields=synopsis,mean,media_type,status,rating`
                axios.get(url, {
                    
                    // withCredentials: false,
                    headers:{
                        // 'Access-Control-Allow-Origin': '*',
                        'X-MAL-CLIENT-ID' : process.env.X_MAL_CLIENT_ID,
                        'Content-Type' : 'application/json; charset=UTF-8',
                        'Accept' : 'application/json'
                    }
                }).then(response => this.anime_res_mal = response.data.data)
                .catch(error =>{
                    console.log(error)
                })
                    
            },
           
        },
        // computed:{
        //         change_page(){
        //             return this.get_animes_mal(this.currentPage)
        //         }
        //     },
        watch: {
            anime_res_mal: function update(){
                this.anime_res_mal.node++
            },
            currentPage: function update(newCurrentPage){
                this.get_animes_mal(newCurrentPage);
            }
        },
    }

   
</script>
<template src="./CardAnime.html">
    
</template>

<style scoped>
    *{  font-family: 'Roboto', sans-serif;
    font-weight: 300;
        margin: 0;
        padding: 0;
    }
</style>