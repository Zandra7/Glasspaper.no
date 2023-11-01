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

.container{
    display: flex;
    justify-content: center;
    margin: auto;
    gap: 39px;
    margin-top: 39px;
    max-width: 100%;
}
.pic1{
    max-width: 460px;
    height: 320px;
}

.pic2{
   max-width: 320px;
   height: 320px; 
}
.pic3{
    max-width: 320px;
    height:320px;
}

@media(max-width: 1170px){
    .container{
    display: flex;
    justify-content: center;
    margin: auto;
    gap: 39px;
    margin-top: 39px;
}
.pic1{
    max-width: 460px;
    height: 320px;
}

.pic2{
   max-width: 320px;
   height: 320px; 
}
.pic3{
    max-width: 340px;
    height:320px;
}
}


</style>