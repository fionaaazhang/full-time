<template>
  <div>
    <van-button type="primary">提示</van-button>
    <h2>为避免后期合并代码的诸多麻烦</h2>
    <h1>开始写代码前请先阅读文档 命名规范.txt</h1>
    <h2>并认真执行</h2>
    
  </div>
</template>
<script>
export default {
  data(){
    return {
      test:[]
    }
  },
  created(){
    this.getlist()
  },
  methods: {
    getlist(){
      this.$http.get('home/getBanners').then(result=>{
        //console.log(result);
        this.test = result.body.data
        
      })
    }
  }
}
</script>
