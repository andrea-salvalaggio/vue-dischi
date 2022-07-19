<template>
    <div class="card">
        <img :src="album.poster" class="card-img-top" :alt="album.author">
        <div class="card-body">
            <h3> {{ album.title }} </h3>
            <p class="card-text"> {{ album.author }} </p>
            <p> {{ album.year }} </p>
        </div>
    </div>
</template>

<script>
export default {
    props: ['album'],
}
</script>

<style>

</style>