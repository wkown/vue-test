<template>
    <div >
        <div class="title">{{title}}</div>
        <div class="msg">{{msg}}</div>
    </div>
</template>

<script>
    export default {
        name: "TestAttribute",
        props:{
            msg: String,
            title:String
        }
    }
</script>

<style scoped>

</style>