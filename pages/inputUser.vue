<template>
  <div class="first-child">
    <h3>Form User</h3>
    <div class="form-group">
      <label for="usr">Name:</label>
      <input type="text" class="form-control" v-model.lazy="user.name">
    </div>
    <div class="form-group">
      <label for="pwd">Password:</label>
      <input type="password" class="form-control" v-model.number="user.password">
    </div>
    <div class="form-group">
      <label for="pwd">Email:</label>
      <input type="text" class="form-control" v-model.number="user.email">
    </div>
    <button class="btn btn-primary" @click="showdata()">Submit></button>
        <div>User Name: {{user.name}}</div>
        <div>Password: {{user.password}}</div>
        <div>Email: {{user.email}}</div>
  </div>
</template>
<script>
export default {
  data(){
    return{
      user:{  
        name:'',
        password:'',
        email:''
      }
    }
  },
   methods:{
    showdata(){
      console.log(this.user)
    }
  }
}
</script>

<style scoped>
.first-child{
margin: auto;
max-width: 600px;}
</style>