<template>
  <div class="container">
    <h3>Nhập điểm của bạn:</h3>
    <input
      v-model.number="score"
      type="number"
      placeholder="Nhập điểm trung bình"
    />

    <p v-if="!score">Vui lòng nhập điểm.</p>
    <p v-else-if="score < 0" style="color: red">
      Điểm Trung Bình không được nhỏ hơn 0
    </p>
    <p v-else-if="score > 10" style="color: red">
      Điểm Trung Bình không được lớn hơn 10
    </p>
    <p v-else>Xếp loại: {{ rank }}</p>
  </div>
</template>

<script setup>
import { computed, ref } from "vue";

const score = ref(null);

// Xếp loại dựa trên điểm nhập
const rank = computed(() => {
  if (score.value === null || score.value === "") return ""; // Không xử lý nếu không nhập
  if (score.value < 5.0) return "Yếu";
  if (score.value >= 5.0 && score.value < 6.5) return "Trung bình";
  if (score.value >= 6.5 && score.value < 8.0) return "Khá";
  if (score.value >= 8.0 && score.value < 9.0) return "Giỏi";
  return "Xuất sắc";
});
</script>

<style scoped></style>
