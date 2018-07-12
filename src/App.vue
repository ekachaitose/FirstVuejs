<template>
<div id="app">
  <img src="./assets/logo.png">
  <h1>{{ msg }}</h1>
  <h2>{{ test }}</h2>
  <el-container>
    <el-header>
      <el-select v-model="value" placeholder="Select">
        <el-option v-for="item in options" :key="item.value" :label="item.label" :value="item.value">
        </el-option>
      </el-select>
    </el-header>
    <el-main>
      <el-row :gutter="10">
        <el-col :sm='2'>
          <span class="demo-input-label">Using attributes</span>
        </el-col>
        <el-col :sm='4'>
          <el-input placeholder="Pick a date" suffix-icon="el-icon-date" v-model="input2">
          </el-input>
        </el-col>
        <el-col :sm='4'>
          <el-input placeholder="Type something" prefix-icon="el-icon-search" v-model="input21">
          </el-input>
        </el-col>
      </el-row>
      <el-row  :gutter="10">
        <el-col :sm='2'>
          <span class="demo-input-label">Using slots</span>
        </el-col>
        <el-col :sm='4'>
          <el-input placeholder="Pick a date" v-model="input22">
            <i slot="suffix" class="el-input__icon el-icon-date"></i>
          </el-input>
        </el-col>
        <el-col :sm='4'>
          <el-input placeholder="Type something" v-model="input23">
            <i slot="prefix" class="el-input__icon el-icon-search"></i>
          </el-input>
        </el-col>
      </el-row>

    </el-main>
  </el-container>
</div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      msg: 'Hello world',
      test: 'YOOOOOOOOOOOOOOO',
      options: [{
        value: 'Option1',
        label: 'Option1'
      }, {
        value: 'Option2',
        label: 'Option2'
      }, {
        value: 'Option3',
        label: 'Option3'
      }, {
        value: 'Option4',
        label: 'Option4'
      }, {
        value: 'Option5',
        label: 'Option5'
      }],
      value: '',
      input2: '',
      input21: '',
      input22: '',
      input23: ''
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
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
</style>
