<template>
  <div id="app">
    <my-input/>
   <my-button  
   color="white" 
    background= "darkslateblue"
    :disabled="!valid" />
  </div>
</template>

<script>
import MyButton from './components/MyButton.vue'
import MyInput from './components/MyInput.vue'

export default {
  components: {
    MyButton,
    MyInput
  },
  data(){
    return{
      valid: true
    }
  }
}
</script>

<style scoped>


</style>
