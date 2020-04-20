<template>
    <button v-on:click="onClick">You clicked me {{ count }} times.</button>
</template>

<script>
    export default {
        name: "ButtonCounter",
        data:function(){
            return {
                count: 0
            }
        },
        methods:{
            onClick:function () {
                this.count++;
                this.$emit('counter-click',this.count);
            }
        }
    }
</script>

<style scoped>

</style>