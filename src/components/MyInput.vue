<template>
<div class="input-wapper">
  <div class="label">
    <label :for="name">{{ name }}</label>
    <div class="error">{{ error }}</div>
  </div>
  <input  :id="name" type="text" v-model="value">
</div>
</template>

<script>


export default {

  props:{
    name: {
      type: String,
      required : true
    },
    rules: {
      type: Object
    }
  },
  data(){
    return{
      value: ''
    }
  },
  computed: {
    error() {
      if (this.rules.required && this.value.length === 0) {
        return 'required'
      }
      
      if (this.rules.min && this.value.length < this.rules.min) {
        return  `minimum length is $(this.rules.min) `
      }
            return 'hey'
    }
  }
}
</script>


<style scoped>

  .input-wrapper{
    display: flex;
    flex-direction: column;
  }

  input{
    background: none;
    color: black;
    border-radius: 5px;
    padding: 10px;
    font-size: 16px;
    border: 1px solid silver;
    margin: 5px 0;
  }


  .error{
    color: red;
  }

  .label{
    display: flex;
    justify-content: space-between;
  }

</style>