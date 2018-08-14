<template>
    <div class="home">
      <allheader @addDoing="handledo"></allheader>
      <list :doingarr="doingarr">
        <div slot="listtitle">正在进行</div>
        <div slot="nums">2</div>
      </list>
      <list>
        <div slot="listtitle">已经完成</div>
        <div slot="nums">2</div>
      </list>
    </div>
</template>
<script>
  import allheader from './components/header'
  import list from './components/list'
    export default {
      components:{
        allheader,
        list
      },
      data(){
        return{
         doingarr:[]
      }
      },
      methods:{
        handledo(data){
        let title=data
         let addto={
            isDone:false,
            title,
         }
         this.doingarr.unshift(addto)
          console.log(this.doingarr)
        }
      }

    }
</script>

<style scoped>

</style>
