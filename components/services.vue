<template>
    <div>
      <div class="container">
        <div class="pic1"> 
          <div class="content">
            <h3>Bemanning og rekruttering</h3>
            <p>Vi finner og kurser riktige kandidater for deg</p>
          </div>
        </div>
        <div class="pic2">
          <div class="content">
            <h3>Konsulenttjenester</h3>
            <p>Enkeltkonsulenter eller hele prosjekter</p>
          </div>
        </div>
        <div class="pic3">
          <div class="content">
            <h3>Programvare</h3>
            <p>Programvare for nanolearning og compliance</p>
          </div>
        </div>
        <!-- <img src="~/public/images/Picture1.png" class="pic1">
        <img src="~/public/images/Picture2.png" class="pic2">
        <img src="~/public/images/Picture3.png" class="pic3"> -->
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
    gap:  3.33%; 
    margin-top: 20px;
    max-width: 1170px; 
    max-width: 100%;
    color: white;
    border-bottom: rgb(204, 204, 204, 1) solid;
    width: 1172px;
    padding-bottom: 83px;
  }
  
  .pic1 {
    display: flex;
    background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 1)), url('~/public/images/Picture1.png');
    max-width: 28.75rem;
    background-size: cover;
  }
  .pic1:hover, .pic2:hover, .pic3:hover {
    box-shadow: 4px 2px 8px 2px rgba(0, 0, 0, 0.70);
  }

  .pic2 {
    background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 1)), url('~/public/images/Picture2.png');
    max-width: 20rem;
    background-size: cover;

  }
  
  .pic3 {
    background-image: linear-gradient(rgba(0, 0, 0, 0.1), rgba(0, 0, 0, 1)), url('~/public/images/Picture3.png');
    max-width: 20rem;
    background-size: cover;
  }

  .content{
    padding: 9.94rem 2.48rem 4.94rem 0.83rem;
    cursor: pointer;
  }

  .pic1 .content {
    padding: 10rem 3.83rem 3.94rem 0.96rem;
  }

  h3 {
    font-size: 1.5rem;
    font-weight: 500;
    text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.75);
  }

  p {
    font-size: 1.125rem;
    font-weight: 400;
    text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.75);
  }

  .line{
    border-bottom: rgb(204, 204, 204, 1) solid;
    width: 1172px;
  }
  
  @media (max-width: 1170px) {
    .container {
      gap:  3.33%;
    }
   .pic1 {
      max-width: 28.75rem;
    }
  
    .pic2 {
      max-width: 20rem;
    }

    .pic3 {
      max-width: 20rem;
    }
  }
  
  @media (max-width: 750px) {
    .container {
      display: grid;
      gap:  2.33%;
      grid-template-areas: 
      "a a"
      "b c";
      max-width: 700px;
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
    min-height: 100%;
    height: auto;
  }
  
  .pic3 {
    max-width: 100%;
    height: auto;
    grid-area: c;
    min-height: 100%;
    height: auto;
  }
  }


  </style>