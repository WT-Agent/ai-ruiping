<template>
  <div class="glass-card ticker-card">
    <div class="ticker-wrapper">
      <div v-for="(item, index) in tickerItems" :key="index" class="ticker-item">
        <span>{{ item.text }}</span>
        <span style="color: var(--success-color); font-weight: bold;">[生成完成]</span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const tickerItems = ref([
  {
    "text": "用户 136****9911 解构了“对齐颗粒度与形成闭环”的大厂黑话"
  },
  {
    "text": "用户 188****3322 锐评了“用花呗分期买名牌包”的消费主义陷阱"
  },
  {
    "text": "用户 132****7700 完成了对“表演式加班与朋友圈晒电脑”的毒舌总结"
  },
  {
    "text": "用户 153****4411 生成了知识付费课程“3天掌握百万变现”的套路拆解"
  },
  {
    "text": "用户 177****6688 取得了人间清醒反职场 PUA 护身符说辞"
  }
]);
</script>
