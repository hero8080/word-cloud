<template>
  <div class="tagcloud">
    <a class="b01 co01" href="#">TaoBao</a>
    <a class="b02 co02" href="#">TaoBao</a>
    <a class="b03 co05" href="#">TaoBao</a>
    <a class="b04 co02" href="#">TaoBao</a>
    <a class="b03 co05" href="#">TaoBao</a>
    <a class="b02 co06" href="#">TaoBao</a>
    <a class="b03 co07" href="#">TaoBao</a>
    <a class="b04 co01" href="#">TaoBao</a>
    <a class="b03 co02" href="#">TaoBao</a>
    <a class="b04 co03" href="#">TaoBao</a>
    <a class="b03 co04" href="#">TaoBao</a>
    <a class="b04 co05" href="#">TaoBao</a>
    <a class="b04 co06" href="#">TaoBao</a>
    <a class="b02 co07" href="#">TaoBao</a>
    <a class="b03 co01" href="#">TaoBao</a>
    <a class="b04 co02" href="#">TaoBao</a>
    <a class="b03 co01" href="#">TaoBao</a>
    <a class="b03 co06" href="#">TaoBao</a>
    <a class="b03 co05" href="#">TaoBao</a>
    <a class="b04 co06" href="#">TaoBao</a>
    <a class="b03 co05" href="#">TaoBao</a>
    <a class="b04 co06" href="#">TaoBao</a>
    <a class="b03 co05" href="#">TaoBao</a>
    <a class="b04 co06" href="#">TaoBao</a>
    <a class="b03 co05" href="#">TaoBao</a>
    <a class="b04 co06" href="#">TaoBao</a>
    <a class="b03 co05" href="#">TaoBao</a>
    <a class="b04 co06" href="#">TaoBao</a>
    <a class="b03 co05" href="#">TaoBao</a>
    <a class="b04 co06" href="#">TaoBao</a>
  </div>
</template>

<script lang="ts" setup>
import { ref, onMounted } from "vue";
import wordCloud from "./lib/wordCloud";

const data = ref([
  "TaoBao",
  "TaoBao",
  "TaoBao",
  "TaoBao",
  "TaoBao",
  "TaoBao",
  "TaoBao",
  "TaoBao",
]);

onMounted(() => {
  wordCloud({
    selector: ".tagcloud",
    fontsize: 16,
    radius: 90,
    mspeed: "normal",
    ispeed: "slow",
    direction: 135,
    keep: false,
  });
});
</script>

<style scoped>
.tagcloud {
  width: 100%;
  height: 100%;
  position: relative;
  visibility: hidden;
}

.tagcloud a {
  display: block;
  border-radius: 50%;
  color: #fff;
  font-weight: bold;
  font-size: 16px;
  text-decoration: none;
  text-align: center;
}

.b01 {
  width: 130px;
  height: 130px;
  line-height: 130px;
}

.b02 {
  width: 110px;
  height: 110px;
  line-height: 110px;
}

.b03 {
  width: 80px;
  height: 80px;
  line-height: 80px;
}

.b04 {
  width: 50px;
  height: 50px;
  line-height: 50px;
}

.co01 {
  background: rgba(61, 134, 244, 0.9);
}

.co02 {
  background: rgba(29, 231, 255, 0.9);
}

.co03 {
  background: rgba(255, 193, 99, 0.9);
}

.co04 {
  background: rgba(213, 107, 170, 0.9);
}

.co05 {
  background: rgba(255, 181, 21, 0.9);
}

.co06 {
  background: rgba(31, 218, 75, 0.9);
}

.co07 {
  background: rgba(219, 67, 231, 0.9);
}
</style>
