<template>
<div class="background">
        <div class="container">
            <div class="a">Glasspaper deler</div>
            <div class="b">Konsernledelse</div>
            <div class="c">Privacy and cookie</div>
            <div class="d">Ofte stilte spørsmål</div>
            <div class="e">Våre lokasjoner</div>
            <div class="f">Legal Terms of Service</div>
            <div class="g">Våre selskaper</div>
            <div class="h">ikoner</div>
            <div class="i">Copyright og Trademark</div>
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
.background{
    background-color: rgba(67, 67, 67,1)
}

.container{
    color: white;
    display:grid;
    grid-template-columns: 2fr 4fr 1fr;
    grid-template-areas:
    "a b c"
    "d e f"
    "g h i";
    padding-top: 65px;
    padding-bottom: 77px;
    margin-top: 83px;
    margin-left: auto;
    margin-right: auto;
    max-width: 1170px;
}

.a, .d, .g{
    font-weight: 700;
    padding-top: 35px
}

.b, .e, .h{
    font-weight: 700;
    padding-top: 35px
}

.c, .f, .i{

    font-weight: 400;
    padding-top: 35px
}

@media(max-width:1000px){
    .container{
    color:brown;
    display:grid;
    grid-template-rows: auto auto auto auto auto auto auto auto auto;
    grid-auto-flow:column;
    font-size: 18px;
}
}

</style>