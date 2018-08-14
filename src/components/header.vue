<template>
  <div class="header">
    <div class="content">
      <div class="container clearfix">
      <div class="title">
        TodoList
      </div>
      <div class="header-search">
        <input type="text" placeholder="添加ToDo" v-model="title" @keyup.enter="handleadd" >
        <button @click="handleadd">ADD</button>
      </div>
      </div>
    </div>
  </div>

</template>

<script>
    export default {

      }
</script>

<style scoped>
  .clearfix:after{
    content:"";
    display: block;
    clear: both;
  }
  .content{
    height: 52px;
    background: #323232;
    position: relative;
  }

  .container{
     width: 600px;
     height: 30px;
     color: #fff;
     background: #323232;
    position: absolute;
    top: 50%;
    left: 50%;
    margin-top: -15px;
    margin-left: -300px;
  }
  .title{
    float: left;
    font-size: 20px;

  }
  .header-search{
    float: right;
    width: 450px;
  }
  .header-search input{
    width: 300px;
    height: 30px;
    color: #ccc;
    border-radius: 6px;
  }
  .header-search button{
    color: #fff;
    width: 100px;
    height: 30px;
    background: #ccc;
    border: 1px solid #ccc;
    border-radius: 8px;
  }
</style>
