<template>
  <div :class="{element: atomicNumber, 'empty-space': isEmpty}">
    <span class="atomic-number">{{ atomicNumber }}</span>
    <span class="atomic-mass">{{ atomicMass }}</span>
    <h1 class="symbol">{{ symbol }}</h1>
    <span class="name">{{ name }}</span>
  </div>
</template>

<script>
//import $ from 'jquery'

export default {
  name: 'Element',
  props: {
    isEmpty: Boolean,
    atomicNumber: Number,
    symbol: String,
    name: String,
    atomicMass : Number,

  },
  created: function(){
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  *{
    user-select: none;
  }
  
  .element{
    width: 80px;
    height: 80px;
    border: 2px solid rgba(0, 155, 194, 0.555);
    background-color: rgba(0, 176, 230, 0.603);
    
    margin: 2px;
    transition: 0.08s;
  }
  .element *{
    color: rgb(0, 0, 0);
  }
  .element:hover{
    transform: scale(2, 2);
  }
  .empty-space{
    width: 80px;
    height: 80px;
    border: 2px solid rgba(0, 0, 0, 0);
    background-color: rgba(0, 176, 230, 0);
    margin: 2px;
  }
  .atomic-number{
    font-size: 12pt;
    font-weight: bold;
    position: relative;
    left: -15%;
    top: 0%;
    margin: 2px;
  }
  .atomic-mass{
    font-size: 8pt;
    font-weight: lighter;
    text-align: right;
    position: relative;
    right: -15%;
    top: 0%;
    margin: 2px;
  }
  .symbol{
    font-size: 18pt;
    font-weight: bolder;
    left: 50%;
    top: 50%;
    margin: 5px;
  }
  .name{
    font-size: 10pt;
    font-weight: normal;
    left: 50%;
    bottom: 0%;
    margin: 8px;
  }
</style>
