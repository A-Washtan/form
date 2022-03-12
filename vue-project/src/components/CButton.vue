<script>
export default {
    props:{
       text: {type: String, required: true},
       color: {type: String},
       background: {type: String},
       disabled: {type: Boolean, requered: true},
    }
};
</script>

<template>
 <button
 :style="{color, background}"
 :disabled="disabled">
     {{text}}</button>
</template>

<style scoped>
button:disabled {
  opacity: .5;  
}
</style>