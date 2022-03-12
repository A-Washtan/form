<script>
import { stringifyQuery } from "vue-router";

export default{
    props: {
        name: {
            type: String,
            required: true
        },
        type: {
            type: String,
            required: true
        },
        value: {
            type: String,
        } ,
        rules: {
           type: Object,
           required: true 
        }
        },
        methods: {
           input(e) {
              this.$emit('onUpdate',{
                  name: this.name,
                  value: e.target.value
              })
              console.log(this.validate(e.target.value))
           },
           validate(value){
             if (this.rules.required && !value){
                 return 'required'
             }  
             if(this.rules.min && value.length < this.rules.min){
                 return `${this.name}>يجب ادخال ${this.rules.min}`
             }
           }
        }
    }

</script>

<template>
<div>
   <label :for="name">{{name}}</label> 
   <input :type="type" id="name" :value="value"
   @input="input"
   >
   </div>
</template>

<style scoped>

</style>