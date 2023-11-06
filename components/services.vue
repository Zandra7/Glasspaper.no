<template>
  <div>
    <div class="container">
      <img src="~/public/images/Picture1.png" class="pc1">
      <img src="~/public/images/Picture2.png" class="pic2">
      <img src="~/public/images/Picture3.png" class="pic3">
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  margin: auto;
  gap: 39px; /* Reduced the gap for responsiveness */
  margin-top: 20px; /* Reduced the margin for responsiveness */
  max-width: 1170px; /* Make the container responsive */
  width: 100%; /* Set a percentage-based width for the container */
}

.pic1 {
  max-width: 460px;; /* Set a max-width for each image based on one-third of the container width */
  height: auto; /* Maintain aspect ratio */
}

.pic2 {
  width: 320px;
  height: auto;
}

.pic3 {
  max-width: 320px;
  height: auto;
}

@media (max-width: 1170px) {
    .container {
  flex-wrap: wrap;
  display: flex;
  justify-content: center;
  margin: auto;
  gap: 39px; /* Reduced the gap for responsiveness */
  margin-top: 20px; /* Reduced the margin for responsiveness */
  max-width: 1170px; /* Make the container responsive */
  width: 100%; /* Set a percentage-based width for the container */
}

.pic1 {
  max-width: 460px;; /* Set a max-width for each image based on one-third of the container width */
  height: auto; /* Maintain aspect ratio */
}

.pic2 {
  width: 320px;
  height: auto;
}

.pic3 {
  max-width: 320px;
  height: auto;
}
}
</style>