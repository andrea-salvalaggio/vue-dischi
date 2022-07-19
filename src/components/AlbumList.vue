<template>
    <div>
        <div class="row">
            <AlbumCover class="card-container" v-for="album in albums" :key="album.index" :album="album"/>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
import AlbumCover from './AlbumCover.vue'

export default {

    data: function(){
        return{
            albums: [],
        }
    },

    components: {
        AlbumCover,
    },

    methods: {
        getAlbumCover(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((result) => {
                console.log(result.data.response)
                this.albums = result.data.response;
            })
            .catch((error) => {
                console.warn(error);
            })
        }
    },

    created(){
        this.getAlbumCover();
    }
}
</script>

<style lang="scss" scoped>
    .card-container{
        width: calc((100% / 5) - 20px);
        margin: 10px
    }
    
</style>