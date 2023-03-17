<script setup lang="ts">
import { ref } from "vue";
const imgAttributes = ref({
  src: "/images/logo.svg",
  alt: "Vueのロゴ1",
  width: 76,
  height: 74
});


const url = ref("https://vuejs.org/");
const isSendButtonDisabled = ref(true);

const widthOrHeight = ref("height");
const widthOrHeightValue = ref(50);



</script>

<template>
  <p><img v-bind="imgAttributes"></p>

  <p><a v-bind:href="url" target="_blank">Vue.jsのサイト</a></p>
  <p><a :href="url" target="_blank">Vue.jsのサイト(省略系)</a></p>
  <p><a v-bind:href="url + 'guide/introduction.html'" target="_blank">Vue.jsガイドのページ</a></p>
  <p><button type="button" v-bind:disabled="isSendButtonDisabled">送信</button></p>
  <p><img alt="vueLogo" src="./assets/logo.svg" v-bind:[widthOrHeight]="widthOrHeightValue"></p>
</template>
