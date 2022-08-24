<template>
    <header class="container-fluid">
        <nav class="container d-flex justify-content-evenly align-items-center py-2">
            <div class="my_height">
                <img src="../assets/img/dc-logo.png" alt="#">
            </div>
            <div>
                <ul class="d-flex justify-content-center align-items-center">
                    <li><a href="#">CHARACTERS</a></li>
                    <li><a href="#">COMICS</a></li>
                    <li><a href="#">MOVIES</a></li>
                    <li><a href="#">TV</a></li>
                    <li><a href="#">GAMES</a></li>
                    <li><a href="#">COLLECTIBLES</a></li>
                    <li><a href="#">VIDEOS</a></li>
                    <li><a href="#">FANS</a></li>
                    <li><a href="#">NEWS</a></li>
                    <li><a href="#">SHOP</a></li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'HeaderComics'
}
</script>

<style scoped lang="scss">
    li{
        padding: 0 10px;
        list-style: none;
        a{
            text-decoration: none;
            font-size: small;
            color:black
        }
    }
</style>