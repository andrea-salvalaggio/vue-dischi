<template>
    <header class="d-flex align-items-center">
        <div class="container-fluid">
            <div class="row">
                <div class="col-12">
                    <div class="logo-container">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/7/75/Spotify_icon.png" alt="Spotify Logo">
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {

}
</script>

<style lang="scss">

    header{
        height: 70px;
        background-color: #2e3a46;
    }

    .logo-container{
        width: 50px;
        height: 50px;

        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }

</style>