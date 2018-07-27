<template>
    <div id="testapp">
        <h1 v-if="txtInput=='yes'||txtInput==''">hello</h1>
        <input :v-model="txtInput" >

    </div>
</template>
<script>
export default {
     name: "testapp",
   
    data() {
            return {
                txtInput:"hhh"
            }
    }
    
}
</script>
