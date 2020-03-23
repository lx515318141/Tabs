<template>
  <div id="app">
    <Hello />
    <tabs :currentIndex='currentIndex' @changeTab="changeTabHandler">
      <tab tabName="tab1" index='1'>
        <div>
          内容1
        </div>
      </tab>
      <tab tabName="tab2" index='2'>
        <div>
          内容2
        </div>
      </tab>
      <tab tabName="tab3" index='3'>
        <div>
          内容3
        </div>
      </tab>
    </tabs>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      currentIndex:"1"
    }
  },
  methods:{
    changeTabHandler(index){
      this.currentIndex = index
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
</style>
