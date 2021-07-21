<template>
  <draggable style="max-width: 400px" v-model="slides" item-key="id">
    <template #item="{element}">
      <slide :title="element.title" />
    </template>
  </draggable>
</template>

<script>
import { reactive, toRefs } from 'vue';
import draggable from "vuedraggable";
import Slide from './components/Slide'

export default {
  name: 'App',
  components: {
    draggable,
    Slide
  },
  setup(){
    const state = reactive({
      slides: [
        {
          title: "Slide1",
          id: 1,
        },
        {
          title: "Slide2",
          id: 2
        }
      ]
    })

    return {
      ...toRefs(state)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
