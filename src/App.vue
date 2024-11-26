<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import Bai1 from "./components/Bai1.vue";
import Bai2 from "./components/Bai2.vue";
import Bai3 from "./components/Bai3.vue";
import Bai4 from "./components/Bai4.vue";
</script>

<template>
  <ul class="nav nav-tabs"role="tablist">
<li class="nav-item">
<a class="nav-link active"data-bs-toggle="tab"href="#home">Bài 1</a>
</li>
<li class="nav-item">
   <a class="nav-link"data-bs-toggle="tab"href="#contact">Bài 2</a>
</li>
<li class="nav-item">
   <a class="nav-link"data-bs-toggle="tab"href="#bai3">Bài 3</a>
</li>
<li class="nav-item">
   <a class="nav-link"data-bs-toggle="tab"href="#bai4">Bài 4</a>
</li>
</ul>
<!-- Tab panes -->
<div class="tab-content">
  <div id="home"class="container tab-pane active"><br>
    <Bai1></Bai1>
</div>
<div id="contact"class="container tab-pane fade"><br>
  <Bai2></Bai2>
</div>
<div id="bai3"class="container tab-pane fade"><br>
  <Bai3></Bai3>
</div>
<div id="bai4"class="container tab-pane fade"><br>
  <Bai4></Bai4>
</div>
</div>

  
 
  
  <!-- <Bai2></Bai2> -->
  <!-- <Bai3></Bai3> -->
  <!-- <Bai4></Bai4>  -->
</template>

<style scoped></style>
