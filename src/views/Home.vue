<template>
<div class = 'screen'>
  
  
  <div>
    <div id = 'topBox'>TopBox</div>
    <div class = 'boxWrap'>
      <Box v-for = 'color in colors' :key = 'color.key' :color = 'color.color'></Box>
    </div>
  </div>
  
</div>
  
</template>

<script>
import Box from '../components/Box.vue'
export default {
  components : {
    Box,
  },
  data(){
    return{
      colors : [
        {color : '#ff6161', key : 1},
        {color : '#ffb761', key : 2},
        {color : '#fff961', key : 3},
        {color : '#61ff74', key : 4},
        {color : '#61f9ff', key : 5},
        {color : '#61a8ff', key : 6},
        {color : '#a061ff', key : 7},
      ]
    }
  }

}
</script>

<style>
  *{
    margin : 0;
    padding : 0;
  }
  body{
    /* width: 100vw; */
    height: 100vh;
    /* display: flex; */
    /* align-items:center; */
    /* justify-content: center; */
    background-color: bisque;
  }
  #topBox{
    display: flex;
    align-items: center;
    font-size: 110%;
    padding-left: 4%;
    box-sizing: border-box;
    border-bottom: 1% solid gray;
    background-color: rgb(192, 192, 192);
    font-weight: 900;
    box-shadow: inset 0px -5px 5px -2px rgb(44 44 44);
    /* height: 8.2%; */
  }
  .screen{
    background-color : white;
    width : 440px;
    height : 352px;
    position: absolute;
    top:30%;
    left:50%;
    transform: translate(-50% , -50%);
  }
  .boxWrap{
    display: flex;
    /* flex-direction: row; */
    overflow: auto;
  }
</style>