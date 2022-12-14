<template>
  <div ref="isShowTag" class="bigScreen w-100 flex-row pos-re">

    <img src="../assets/img/22.jpg" class="img" alt="">

    <div ref="rightDetail" class="right-detail">
      <div class="right">
        <img ref="imgDetail" src="../assets/img/22.jpg" class="img-detail" alt="">
        <img ref="imgDetailClone" src="../assets/img/22.jpg" class="img-detailClone" alt="">
      </div>
    </div>

  </div>
</template>
<script setup>
import { createBlockStatement } from '@vue/compiler-core';
import { ref, onMounted, onUpdated, onBeforeUpdate } from 'vue';
const screenWidth = ref(document.documentElement.clientWidth)
const screenHeight = ref(document.documentElement.clientHeight)
const isPortraitScreen = ref(false)
const isShowTag = ref()
const viewWidth = ref()
const imgDetail = ref();
const imgDetailClone = ref();
const MyMar = ref()
const speed = ref(10)
const rightDetail = ref()


/* 长图滚动 */
const MarQuee = () => {
  if (imgDetailClone.value.offsetHeight) {
    if (imgDetailClone.value.offsetHeight - rightDetail.value.scrollTop < 4) {
      rightDetail.value.scrollTop -= imgDetail.value.offsetHeight
    } else {
      rightDetail.value.scrollTop++
    }
  }
}

const getScreenSize = () => {
  screenWidth.value = document.documentElement.clientWidth
  screenHeight.value = document.documentElement.clientHeight
  // console.log('screenWidth.value', screenWidth.value)
  // console.log('screenHeight.value', screenHeight.value)
}

console.log('screenWidth.value', screenWidth.value)
console.log('screenHeight.value', screenHeight.value)

onUpdated(() => {
  console.log(isPortraitScreen.value);
  if (screenWidth.value < screenHeight.value) {
    isPortraitScreen.value = true
    console.log('isPortraitScreen.value', isPortraitScreen.value)
    isShowTag.value.className = "flex-col";
  }
  else {
    isShowTag.value.className = 'flex-row';
  }
  // window.addEventListener('resize', getScreenSize)
  // if (!isPortraitScreen.value) {
  //   isShowTag.value.className = 'bigScreen w-100 flex-row pos-re';
  // } else {
  //   isShowTag.value.className = "bigScreen w-100 flex-col pos-re";
  // }
});

onBeforeUpdate(() => {
  console.log(isPortraitScreen.value);
})


onMounted(() => {

  MyMar.value = setInterval(MarQuee, speed.value);
  screenWidth.value = document.documentElement.clientWidth;
  screenHeight.value = document.documentElement.clientHeight;
  console.log('screenWidth.value', screenWidth.value)
  console.log('screenHeight.value', screenHeight.value)


  window.addEventListener('resize', getScreenSize)
})
</script>
<style lang="scss" scoped>
.bigScreen {
  height: 100%;
  overflow: hidden;

  .img {
    // width: 2.56rem;
    // height: 2.56rem;
    height: 100%;
    margin-right: .05rem;
  }

  .right-detail {
    height: 100%;
    overflow: hidden;
    .right {
      // width: 5.12rem;
      height: 100%;

      .img-detailClone{
        margin-top: 0.2rem;
      }
    }
  }


}
</style>