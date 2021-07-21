<template>
  <div class="slide">{{title}}</div>
</template>

<script>
export default {
    props: {
        title: String
    },
    setup(){
        console.log("Slide::setup()")
    }
}
</script>

<style>
    .slide {
        padding: 10px;
        background-color: royalblue;
        color: white;
    }
</style>