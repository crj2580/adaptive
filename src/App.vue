<script setup>
import { ref, onMounted, onUpdated, onBeforeUpdate } from 'vue';
import SacleBox from './components/SacleBox.vue';
import HelloWorld from './components/HelloWorld.vue';
</script>

<template>
  <!-- <div ref="isShowTag" class="bigScreen w-100 flex-row pos-re">

    <img src="./assets/img/22.jpg" class="img" alt="">

    <div class="right">
      <img src="./assets/img/22.jpg" alt="">
    </div>

  </div> -->
  <HelloWorld />
</template>

<style lang="scss" scoped>
.bigScreen {
  // width: 100%;
  height: 100%;
  overflow: hidden;



  // .img {
  //   // height: 2.56rem;
  //   // width: 8rem;
  //   // height: 8rem;
  //   height: 100%;
  // }

  // .right {
  //   height: 100%;
  //   overflow: hidden;
  // }

}

// @media screen and (min-width:769px) {
//   .bigScreen {
//     background-color: blueviolet;
//   }
// }

// @media screen and (max-width:768px) {
//   .bigScreen {
//     // width: 100%;
//     height: 100%;
//     overflow: hidden;



//     .img {
//       // height: 2.56rem;
//       // width: 8rem;
//       // height: 8rem;
//       height: 100%;
//     }

//     .right {
//       height: 100%;
//       overflow: hidden;
//     }

//   }
// }

// @media screen and (max-width:448px) {
//   .bigScreen {
//     // width: 100%;
//     height: 100%;
//     overflow: hidden;
//     flex-direction: column;



//     .img {
//       // height: 2.56rem;
//       // width: 8rem;
//       // height: 8rem;
//       height: 100%;
//     }

//     .right {
//       height: 100%;
//       overflow: hidden;
//     }
//   }
// }

// @media screen and (max-width:384px) {
//   .bigScreen {
//     // width: 100%;
//     // height: 6.4rem;
//     height: 100%;
//     overflow: hidden;
//     flex-direction: column;



//     .img {
//       // height: 2.56rem;
//       // width: 8rem;
//       // height: 8rem;
//       height: 100%;
//     }

//     .right {
//       height: 100%;
//       overflow: hidden;
//     }
//   }
// }

// @media screen and (max-width:320px) {
//   .bigScreen {
//     // width: 100%;
//     // height: 6.4rem;
//     height: 100%;
//     overflow: hidden;
//     flex-direction: column;

//     .img {
//       // height: 2.56rem;
//       // width: 8rem;
//       // height: 8rem;
//       // height: 100%;
//     }

//     .right {
//       height: 100%;
//       overflow: hidden;
//     }
//   }
// }

// .bigScreen {
//   width: 100%;
//   height: 100vh;
//   overflow: hidden;
//   position: relative;
//   font-size: 14px;
//   background-color: black;

//   .main-wraper {
//     user-select: none;
//     height: 800px;
//     width: 800px;
//     margin: 0 auto;
//     background-color: red;
//     background-size: cover;
//     box-sizing: border-box;
//     background-repeat: no-repeat;

//   }
// }
</style>
