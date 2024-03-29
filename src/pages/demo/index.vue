<script setup lang="ts">
definePage({
  name: 'Demo',
  meta: {
    level: 2,
    title: '🎉 Demo',
    i18n: 'home.demo',
  },
})
</script>

<template>
  <div class="demo relative m-[-4rem] text-center">
    <div class="top-bg absolute z-[-1] box-border h-[440px] w-[100%] bg-[#7060E5]" />
    <van-button icon="cross" round type="primary" class="close-btn !mt-20 !border-none !bg-gray" />
    <p class="text-[24px] color-[#eee] font-bold">
      Your Ticket
    </p>
  </div>
</template>

<style lang="less" scoped>
.close-btn {
  width: 35px;
  height: 35px;
}
.top-bg {
  border-bottom-left-radius: 30px;
  border-bottom-right-radius: 30px;
}
</style>
