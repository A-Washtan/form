<script>
export default{
    props: {
        name: {
            type: String,
            required: true
        },
        type: {
            type: String,
            required: true
        }
    }
}
</script>

<template>
<div>
   <label :for="name">{{name}}</label> 
   <input :type="type" id="name">
   </div>
</template>

<style scoped>

</style>