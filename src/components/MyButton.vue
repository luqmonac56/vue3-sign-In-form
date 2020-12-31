<template>
    <button 
    :style = "{background , color }"
    :disabled = "disabled"
    >
        Button
    </button>
</template>

<script>

export default {
    props: {
        color:{
            type: String
        },
        background:{
            type:String
        },
        disabled:{
            type: Boolean
        }

    },
  components: {
    
  }
}
</script>

<style scoped>

button:disabled{
    opacity: .5;
}
button{
    background: none;
    color: black;
    border-radius: 5px;
    padding: 10px 40px;
    font-size: 16px;
    border: none;
    cursor: pointer;
}

button:hover{
    filter: brightness(125%);
}



</style>
