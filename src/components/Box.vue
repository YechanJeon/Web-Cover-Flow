<template>
  <div class = 'box'>
      <div class = 'mainBox' :style = 'style'>

      </div>
      <div class  = 'mainBoxGradient' :style = 'style'>

      </div>
  </div>
</template>

<script>
export default {
    props : {
        color : {
            type : String
        }
    },
    data(){
        return{
            style : {
                'background-color' : '#a061ff'
            }
        }
    },
    created(){
        this.style['background-color'] = this.color
    }

}
</script>

<style>
    .box{
        display: flex;    
        justify-content: center;
        flex-direction: column;
        margin-top: 20px ;
    }
    .mainBox{
        width: 180px;
        height: 180px;
    }
    .mainBoxGradient{
        width: 180px;
        height: 80px;
        opacity: 0.8;
    }

</style>