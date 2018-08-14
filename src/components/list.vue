<template>
    <div>
      <div class="home-content">
        <div class="doing ">
          <div class="doing-top clearfix">
            <div class="doing-title fll">
              <h2>正在进行</h2>
            </div>
            <div class="doingall flr">
              3
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
