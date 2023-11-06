<template>
    <div>
      <div class="container">
        <img src="~/public/images/Picture1.png" class="pic1">
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
    gap: 39px; 
    margin-top: 20px;
    max-width: 1170px; 
    width: 100%;
  }
  
  .pic1 {
    flex: 1;
    max-width: 39.32%;
    height: auto;
  }
  
  .pic2 {
    max-width: 27.35%;
    height: auto;
  }
  
  .pic3 {
    max-width: 27.35%;
    height: auto;
  }
  
  @media (max-width: 1170px) {
    .container {
      gap: 10px;
      margin-top: 10px;
    }
  }
  </style>