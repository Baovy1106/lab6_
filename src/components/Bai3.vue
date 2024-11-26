<template>
  <div class="container mt-5">
    <h1 class="text-center">Kiến thức sức khỏe cộng đồng</h1>
    <div class="row">
      <div class="col-sm-4 mb-3" v-for="(item, index) in items" :key="index">
        <div class="card">
          <img :src="item.image" class="img" alt="Hình anh" width="405px" height="250px"/>
          <div class="card-body">
            <h3 class="card-title">{{ item.title }}</h3>
            <p class="card-text">{{ item.content }}</p>
            <button class="btn btn-info">Xem chi tiết</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import banner1 from "../assets/images/img1.jpg";
import banner2 from "../assets/images/img2.jpg";
import banner3 from "../assets/images/img3.jpg";

const items = [
  {
    title: "8 loại rau củ quả giàu canxi",
    content:
      "Canxi là khoáng chất cần thiết đối với cơ thể người. Có nhiều cách để bổ sung canxi, trong đó bổ sung qua đường ăn uống là cách tốt nhất. Có 8 loại rau củ giàu canxi ...",
    image: banner1,
  },
  {
    title: "Các gia vị tốt cho sức khỏe",
    content:
      "Một số loại gia vị cung cap nhiều polyphenol chống oxy hóa cao hơn các loại gia vị quen thuộc khác. Với một lượng nhỏ các món ăn đã thêm hương thơm và vị hấp dẫn ...",
    image: banner2,
  },
  {
    title: "đậu bổ dưỡng nên dùng",
    content:
      "Đậu lăng, đậu nành, đậu đỏ, đậu đen, đậu phộng, đậu Hà Lan giàu chất xơ, protein cùng nhiều vitamin và khoáng chất giúp giảm lượng đường trong máu, tốt cho tim ...",
    image: banner3,
  },
];
</script>
<style>
.container {
  margin-left: 80px;
}
</style>
