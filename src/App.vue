<template>
  <div id="app">
  
    <img src="./assets/logo.png">
  
    <h1>{{ msg }}</h1>
  
    <el-container>

      <el-form class="styleform" :model="regisForm">  
          <el-row class="spacerow" :gutter="10">
  
            <el-col :sm='7' class="lblright">
  
              <label class="demo-input-label">Name</label>
            </el-col>
  
            <el-col :sm='4'>
  
              <el-input placeholder="input your name" v-model="regisForm.txtName">
  
              </el-input>
  
            </el-col>
  
            <el-col :sm='3' class="lblright">
  
              <label class="demo-input-label">Lastname</label>
  
            </el-col>
  
            <el-col :sm='4'>
  
              <el-input placeholder="input your lastname" v-model="regisForm.txtLastName">
  
              </el-input>
  
            </el-col>
  
          </el-row>
  
          <el-row class="spacerow" :gutter="10">
  
            <el-col :sm='7' class="lblright">
  
              <label class="demo-input-label">E-mail</label>
  
            </el-col>
  
            <el-col :sm='4'>
  
              <el-input placeholder="input your E-mail" v-model="regisForm.txtEmail">
  
              </el-input>
  
            </el-col>
  
            <el-col :sm='3' class="lblright">
  
              <label class="demo-input-label">Phone number</label>
  
            </el-col>
  
            <el-col :sm='4'>
  
              <el-input placeholder="input your Phone number" v-model="regisForm.txtPhone">
  
              </el-input>
  
            </el-col>
  
          </el-row>
            <el-row class="spacerow" :gutter="10">
  
            <el-col :sm='7' class="lblright">
  
              <label class="demo-input-label">Username</label>
  
            </el-col>
  
            <el-col :sm='4'>
  
              <el-input placeholder="input your Username" v-model="regisForm.txtUserName">
  
              </el-input>
  
            </el-col>
  
            <el-col :sm='3' class="lblright">
  
              <label class="demo-input-label">Password</label>
  
            </el-col>
  
            <el-col :sm='4'>
              <el-input placeholder="input your Pasword" v-model="regisForm.txtPassword">
  
              </el-input>
  
            </el-col>
          </el-row>
          <el-row>
            <el-button type="success" v-on:click="onSubmit('regisform')" plain>
              OK
            </el-button>
            <el-button type="danger" plain >
              Clear
            </el-button>
          </el-row>
         
      </el-form>
   
    </el-container>
  
  </div>
</template>

<script>
  export default {
  
    name: "app",
  
    data() {
  
      return {
  
        msg: "Hello world",
       regisForm:{
         txtName: "",
         txtLastName:"",
         txtEmail:"",
         txtPhone:0,
         txtUserName:"",
         txtPassword:""
       }
      };
    },
       methods:{
         onSubmit(form)  {
       alert(JSON.stringify(this.regisForm))
         }
       }
  
  };
</script>

<style>
  #app {
  
    font-family: "Avenir", Helvetica, Arial, sans-serif;
  
    -webkit-font-smoothing: antialiased;
  
    -moz-osx-font-smoothing: grayscale;
  
    text-align: center;
  
    color: #2c3e50;
  
    margin-top: 60px;
  
  }
  
  
  
  h1,
  
  h2 {
  
    font-weight: normal;
  
  }
  
  
  
  a {
  
    color: #42b983;
  
  }
  
  
  
  .lblright {
  
    text-align: right;
  
  }
  
  
  
  .spacerow {
  
    margin-bottom: 10px;
  
  }
  
  
  
  .styleform {
  
    width: 100%;
    background-color: #0777;
    border-radius: 5px;
    padding: 10px 5px;
  
  }
</style>
