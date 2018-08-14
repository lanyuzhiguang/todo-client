<template>
    <div>
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
      <div class="home-content">
        <div class="doing ">
          <div class="doing-top clearfix">
            <div class="doing-title fll">
              <slot name="list-title"></slot>
            </div>
            <div class="doingall flr">
              <slot name="nums"></slot>
            </div>
          </div>
          <div class="doing-content" >
            <div class="doing-item" >
              <input type="checkbox" class="doing-select fll" >
              <span >吃饭</span>
              <button class="doing-btn flr"  >删除</button>
            </div>
          </div>
        </div>
        <div class="finish ">
        <div class="finish-top clearfix">
        <div class="finish-title fll">
        <h2>已经完成</h2>
        </div>
        <div class="finishall flr">
        2
        </div>
      </div>
        <div class="finish-content">
        <div class="finish-item" >
        <input type="checkbox" class="finish-select fll" >
        <span >睡觉</span>
        <button class="finish-btn flr" >删除</button>
        </div>
        </div>
        </div>
      </div>
    </div>
</template>

<script>
    export default {
        name: "quan"
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
.clearfix:after{
  content:"";
  display: block;
  clear: both;
}
.fll{
  float: left;
}
.flr{
  float: right;
}
.home-content{
  width: 600px;
  margin: 0 auto;
}
.doing,.finish{
  padding-top: 10px;
  padding-bottom: 10px;
}
.doingall,.finishall {
  line-height: 30px;
  text-align: center;
  width: 30px;
  height: 30px;
  background: #EAE3E3;
  color: #fff;
  border-radius: 50%;
}
.doing-content,.finish-content{
  padding-top: 20px;
  padding-bottom: 20px;
}
.doing-item,.finish-item{
  margin: 10px;
  padding: 0px 10px 0px 20px;
  width:565px;
  height: 30px;
  border-left:4px solid #1550CB
  border-radius: 4px;
  background: #fff;
  line-height: 30px;
}

.doing-select,.finish-select{
  width: 20px;
  height: 20px;
  margin-top: 5px;
}
.doing-btn,.finish-btn{
  margin-top: 5px;
}

</style>
