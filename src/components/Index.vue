<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        <p>
            Index Page
            <ButtonCounter></ButtonCounter>
        </p>
    </div>
</template>
<script>
    import ButtonCounter from "./widgets/ButtonCounter";

    export default {
        name: 'Index',
        props: {
            msg: String
        },
        components: {
            ButtonCounter
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
