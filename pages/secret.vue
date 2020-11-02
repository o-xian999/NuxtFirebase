<template>
  <div>
    <h1>This is secret info</h1>
  </div>
</template>

<script>
import { firebase } from '@firebase/app'
import '@firebase/auth'
export default {
  asyncData({req, redirect}){
    if(process.server){
      
    } else {
      let user = firebase.auth().currentUser;
      if(!user){
      redirect("/login")
    }
    }
    
    
  }
}
</script>

<style lang="scss" scoped>

</style>