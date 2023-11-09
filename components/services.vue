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
     </div>
     <hr>
   </div>
</template>
 
 <script setup>
 </script>
 
<style scoped>
 .container {
   display: flex;
   justify-content: center;
   flex-wrap: wrap;
   margin: auto;
   gap:  35px; 
   margin-top: 20px;
   max-width: 1170px; 
   width: 100%;
   color: white;
   padding-bottom: 83px;
 }
 
 .pic1:hover, .pic2:hover, .pic3:hover {
   box-shadow: 4px 2px 8px 2px rgba(0, 0, 0, 0.70);
 }
 
 .pic1 {
   background-image: linear-gradient(180deg, rgba(0, 0, 0, 0.10) 43.23%, #000 100%), url('~/public/images/Picture1.png');
   width: 460px;
 }
 .pic2 {
   background-image: linear-gradient(180deg, rgba(0, 0, 0, 0.10) 43.23%, #000 100%), url('~/public/images/Picture2.png');
   width: 320px;
 }
 
 .pic3 {
   background-image: linear-gradient(180deg, rgba(0, 0, 0, 0.10) 43.23%, #000 100%), url('~/public/images/Picture3.png');
   width: 320px;
 }
 .pic1, .pic2, .pic3 {
   background-size: cover;
   background-repeat: no-repeat;
   height: 320px;
 }
 .content {
   cursor: pointer;
 }
 h3 {
   padding: 191px 133.62px 17px 15.33px;
   margin: 0;
   font-size: 1.5rem;
   font-weight: 500;
   text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.75);
 }
 p {
   padding: 0 61.33px 0 15.33px;
   margin: 0;
   font-size: 1.125rem;
   font-weight: 400;
   text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.75);
 }
 
 hr {
   max-width: 1170px;
 }
 @media (max-width: 1175px) {
   hr {
     margin: 0 2rem;
   }
 }
 @media (max-width: 1170px) {
   .container {
     gap:  2.33%;
   }
 
   .pic2 {
     max-width: 20rem;
   }
   .pic3 {
     max-width: 20rem;
   }
 }
 
 @media (max-width: 1153px) {
   .container {
     display: grid;     
     gap:  2.33%;
     grid-template-areas: 
     "a a"
     "b c";
   }
   .pic1 {
     grid-area: a;
     margin: 0 auto;
     width: 100%;
     background-position: bottom;
 }
 
 .pic2 {
   max-width: 100%;
   grid-area: b;
 }
 
 .pic3 {
   max-width: 100%;
   grid-area: c;
 }
 }
 @media (max-width: 660px) {
   .container {
     grid-template-areas: 
     "a"
     "b"
     "c";
   }
   .pic1 {
     width: 320px;
   }
 }
 @media (max-width: 425px) {
   .pic1, .pic2, .pic3 {
     background-size: cover;
     background-position: center;
     width: 100%;
     height: 320px;
   }
 }
</style>