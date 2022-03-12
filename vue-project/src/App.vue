<script>

import CButton from "./components/CButton.vue"
import CInput from "./components/CInput.vue"

export default {
  components: { 
    CButton,
    CInput 
  },
  data(){
    return{
      valid: false
    }
  },
  methods: {
    onUpdate(data) {
      
    }
  },
  
}
</script>



<template>
<div> 
<c-input
name="الاسم"
type="text"
:rules="{required: true, min: 6}"
@onUpdate="onUpdate"

/>
<c-input
name="كلمة المرور"
type="password"
:rules="{required: true, min: 8}"
@onUpdate="onUpdate"
/>
 <c-button 
text="تسجيل"
color="brown"
background="black"
:disabled="valid"
/>
</div>
</template> 

<style>

</style>
