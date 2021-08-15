<template>
    <img alt="Compasso logo" src="https://compassouol.com/wp-content/uploads/2021/04/Desktop.png.webp">
    <list></list>
</template>

<script>
import List from "./components/List";
export default {
    name: 'App',
    components: {
        List
    }
}
</script>

<style>
body{
    margin: 0;
    background: #242021

}

#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: white;
    margin-top: 60px;
}

#app img{
    margin-bottom: 30px;
}
</style>
