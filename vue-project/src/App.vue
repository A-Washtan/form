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
  }
  
}
</script>



<template>
<div> 
<c-input
name="الاسم"
type="text"
/>
<c-input
name="كلمة المرور"
type="password"
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
