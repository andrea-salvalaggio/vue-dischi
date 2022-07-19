<template>
    <div class="card text-white">
        <img :src="album.poster" class="card-img-top" :alt="album.author">
        <div class="card-body text-center px-0">
            <h5 class="text-uppercase fw-bold mb-3"> {{ album.title }} </h5>
            <p class="card-text m-0"> {{ album.author }} </p>
            <p class="m-0"> {{ album.year }} </p>
        </div>
    </div>
</template>

<script>
export default {
    props: ['album'],
}
</script>

<style lang="scss" scoped>

    .card{
        background-color: #2e3a46;
    }

    p{
        color: #5a5d62;
    }

</style>