<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        <p>
            Index Page
        </p>
      <p><ButtonCounter v-on:onClick="onButtonClick"></ButtonCounter></p>
      <p><ShowMsg title="The Button Click Count:" v-bind:msg="subMsg"></ShowMsg></p>
    </div>
</template>
<script>
    import ButtonCounter from "./widgets/ButtonCounter";
    import ShowMsg from "./widgets/ShowMsg";

    export default {
        name: 'Index',
        props: {
          msg: String
        },
      data: function(){
          return {
            subMsg: 'Wait data ...'
          }
      },
        components: {
          ButtonCounter,
          ShowMsg
        },
      methods:{
        onButtonClick:function (count) {
          this.subMsg = 'You clicked me '+count+' times';
        }
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
