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
    gap:  39px; 
    margin-top: 20px;
    max-width: 1170px; 
    width: 100%;
    border-bottom: rgb(204, 204, 204, 1) solid;
    padding-bottom: 83px;
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

  .line{
    border-bottom: rgb(204, 204, 204, 1) solid;
    width: 1172px;
  }
  
  @media (max-width: 1170px) {
    .container {
      gap:  2.33%;

    }
     .pic1 {
    flex: 1;
    max-width: 37.32%;
    height: auto;
  }
  
  .pic2 {
    max-width: 25.35%;
    height: auto;
  }
  
  .pic3 {
    max-width: 25.35%;
    height: auto;
  }
  }
  
  @media (max-width: 750px) {
    .container {
      display: grid;
      gap:  2.33%;
      grid-template-areas: 
      "a a"
      "b c";

    }
     .pic1 {
    max-width: 100%;
    left: 10px;
    height: auto;
    grid-area: a;
    margin-left: auto;
      margin-right: auto;
      width: 100%;
  }
  
  .pic2 {
    max-width: 100%;
    height: auto;
    grid-area: b;
  }
  
  .pic3 {
    max-width: 100%;
    height: auto;
    grid-area: c;
  }
  }
  </style>