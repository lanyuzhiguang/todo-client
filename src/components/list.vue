<template>
    <div>
      <div class="home-content">
        <div class="doing ">
          <div class="doing-top clearfix">
            <div class="doing-title fll">
              <slot name="listtitle"></slot>
            </div>
            <div class="doingall flr">
              <slot name="nums"></slot>
            </div>
          </div>
          <div class="doing-content" >
            <div class="doing-item" v-for="(doing,index) in doingarr" :key="index">
              <input type="checkbox"
                     class="doing-select fll"
                     @change="handlechange(index)">
              <span >{{doing.title}}</span>
              <button class="doing-btn flr"  @click="handelremove(index)">删除</button>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>

    export default {
      props:{
        doingarr:Array,

      },
      data(){
        return{
          finisharr:[]
        }
      } ,
     methods:{
        handelremove(index){
        this.doingarr.splice(index,1)
        },
       handlechange(index){



       },
     }
    }
</script>

<style scoped>
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
    border-left:4px solid #1550CB ;
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
