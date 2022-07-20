<template>
    <div>
        <div class="row">
            <select class="form-select form-select-lg mb-3" aria-label=".form-select-lg example">
                <option value="rock">Rock</option>
                <option value="pop">Pop</option>
                <option value="jazz">Jazz</option>
                <option value="metal">Metal</option>
            </select>
            <AlbumCover class="card-container py-3" v-for="album in albums" :key="album.index" :album="album"/>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
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
        width: calc((100% / 5) - 30px);
        margin: 15px
    }

</style>