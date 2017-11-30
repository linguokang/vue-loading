<template>
  <div class="vue-loading" v-if="isLoading" :style="{transform: getScale}">
    <div class="img-box" >
      <div :class="[{ loading }, type]" >
        <span :style="{ background: color}"></span>
        <span :style="{ background: color}"></span>
        <span :style="{ background: color}"></span>
        <span :style="{ background: color}"></span>
        <span :style="{ background: color}"></span>
      </div>
      <div class="text">{{text}}</div>
    </div>

  </div>
</template>
<script>

  export default {
    name: 'vue-loading',
    props: {
      isLoading: {
        type: Boolean,
        default: false
      },
      type: {
        type: String,
        default: 'loading1'
      },
      text:{
        type: String,
        default: '加载中...'
      },
      color:{
        type: String,
        default: 'lightgreen'
      },
      scale:{
        type: String,
        default: '1'
      }
    },
    data() {
      return {
        loading:true
      }
    },
    computed: {
      getScale() {
        return "scale("+this.scale+")"
      }
    },
    methods: {

    }
  }
</script>
<style lang="scss" scoped>
  .vue-loading{
    display: flex;
    position: absolute;
    left: 50%;
    top: 50%;
    margin-left: -100px;
    margin-top: -100px;
    height: 200px;
    width: 200px;
    background: rgba(0,0,0,0.6);
    align-items: center;
    justify-content: center;
    border-radius: 20px;
    .img-box{
      height: 200px;
      width: 200px;
      text-align: center;
      img{
        width: 100%;
        height: 100%;
      }
      .text{
        text-align: center;
        margin-top: 20px;
        color: #fff;
      }
    }
  }
  .loading{
    span{
      background: lightgreen;
    }
  }
  .loading1{
    width: 80px;
    height: 40px;
    margin: 0 auto;
    margin-top:80px;
    span{
      display: inline-block;
      width: 8px;
      height: 100%;
      border-radius: 4px;
      -webkit-animation: load1 1s ease infinite;
    }
    @-webkit-keyframes load1{
      0%,100%{
        height: 40px;
      }
      50%{
        height: 70px;
        margin: -15px 0;
      }
    }
    span:nth-child(2){
      -webkit-animation-delay:0.2s;
    }
    span:nth-child(3){
      -webkit-animation-delay:0.4s;
    }
    span:nth-child(4){
      -webkit-animation-delay:0.6s;
    }
    span:nth-child(5){
      -webkit-animation-delay:0.8s;
    }
  }
  .loading2{
    width: 150px;
    height: 15px;
    margin: 0 auto;
    margin-top:80px;
    span{
      display: inline-block;
      width: 15px;
      height: 100%;
      margin-right: 5px;
      border-radius: 50%;
      -webkit-animation: load2 1.04s ease infinite;
    }
    span:last-child{
      margin-right: 0px;
    }
    @-webkit-keyframes load2{
      0%{
        opacity: 1;
      }
      100%{
        opacity: 0;
      }
    }
    span:nth-child(1){
      -webkit-animation-delay:0.13s;
    }
    span:nth-child(2){
      -webkit-animation-delay:0.26s;
    }
    span:nth-child(3){
      -webkit-animation-delay:0.39s;
    }
    span:nth-child(4){
      -webkit-animation-delay:0.52s;
    }
    span:nth-child(5){
      -webkit-animation-delay:0.65s;
    }
  }
  .loading3{
    width: 150px;
    height: 15px;
    margin: 0 auto;
    margin-top:80px;
    span{
      display: inline-block;
      width: 15px;
      height: 100%;
      margin-right: 5px;
      -webkit-transform-origin: right bottom;
      -webkit-animation: load3 1s ease infinite;
    }
    @-webkit-keyframes load3{
      0%{
        opacity: 1;
      }
      100%{
        opacity: 0;
        -webkit-transform: rotate(90deg);
      }
    }
    span:nth-child(1){
      -webkit-animation-delay:0.13s;
    }
    span:nth-child(2){
      -webkit-animation-delay:0.26s;
    }
    span:nth-child(3){
      -webkit-animation-delay:0.39s;
    }
    span:nth-child(4){
      -webkit-animation-delay:0.52s;
    }
    span:nth-child(5){
      -webkit-animation-delay:0.65s;
    }
  }
  .loading4{
    width: 80px;
    height: 40px;
    margin: 0 auto;
    margin-top:80px;
    span{
      display: inline-block;
      width: 8px;
      height: 100%;
      border-radius: 4px;
      -webkit-animation: load4 1.04s ease infinite;
    }
    @-webkit-keyframes load4{
      0%,100%{
        height: 40px;
      }
      50%{
        height: 60px;
        margin-top: -20px;
      }
    }
    span:nth-child(2){
      -webkit-animation-delay:0.13s;
    }
    span:nth-child(3){
      -webkit-animation-delay:0.26s;
    }
    span:nth-child(4){
      -webkit-animation-delay:0.39s;
    }
    span:nth-child(5){
      -webkit-animation-delay:0.52s;
    }
  }
  .loading5{
    width: 150px;
    height: 15px;
    margin: 0 auto;
    margin-top:80px;
    text-align: center;
    span{
      display: inline-block;
      width: 15px;
      height: 100%;
      margin-right: 5px;
      -webkit-animation: load5 1.04s ease infinite;
    }
    .loading span:last-child{
      margin-right: 0px;
    }
    @-webkit-keyframes load5{
      0%{
        opacity: 1;
        -webkit-transform: scale(1.2);
      }
      100%{
        opacity: .2;
        -webkit-transform: scale(.2);
      }
    }
    span:nth-child(1){
      -webkit-animation-delay:0.13s;
    }
    span:nth-child(2){
      -webkit-animation-delay:0.26s;
    }
    span:nth-child(3){
      -webkit-animation-delay:0.39s;
    }
    span:nth-child(4){
      -webkit-animation-delay:0.52s;
    }
    span:nth-child(5){
      -webkit-animation-delay:0.65s;
    }
  }
  .loading6{
    width: 80px;
    height: 80px;
    border-radius: 50%;
    margin: 0 auto;
    margin-top:50px;
    position: relative;
    border:5px solid lightgreen;
    -webkit-animation: turn 2s linear infinite;
    span{
      display: inline-block;
      width: 30px;
      height: 30px;
      border-radius: 50%;
      position: absolute;
      left: 50%;
      margin-top: -15px;
      margin-left: -15px;
    }
    @-webkit-keyframes turn{
      0%{
        -webkit-transform: rotate(0deg);
      }
      100%{
        -webkit-transform: rotate(360deg);
      }
    }
  }
  .loading7{
    width: 150px;
    height: 4px;
    border-radius: 2px;
    margin: 0 auto;
    margin-top:100px;
    position: relative;
    background: lightgreen;
    -webkit-animation: changeBgColor 1.04s ease-in infinite alternate;
    span{
      display: inline-block;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      position: absolute;
      margin-top: -7px;
      margin-left:-8px;
      -webkit-animation: changePosition7 1.04s ease-in infinite alternate;
    }
    @-webkit-keyframes changePosition7{
      0%{
        margin-left: -75px;
      }
      100%{
        margin-left: 71px;
      }
    }
  }
  .loading8{
    width: 150px;
    height: 8px;
    border-radius: 4px;
    margin: 0 auto;
    margin-top:100px;
    position: relative;
    background: lightblue;
    overflow: hidden;
    span{
      display:block;
      width: 100%;
      height: 100%;
      border-radius: 3px;
      -webkit-animation: changePosition 4s linear infinite;
    }
    @-webkit-keyframes changePosition{
      0%{
        -webkit-transform: translate(-150px);
      }
      50%{
        -webkit-transform: translate(0);
      }
      100%{
        -webkit-transform: translate(150px);
      }
    }
  }


</style>
