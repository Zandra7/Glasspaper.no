<template>
    <div class="background">
        <div class="container">
            <div class="a">Glasspaper deler</div>
            <div class="b">Konsernledelse</div>
            <div class="c">Privacy and cookie</div>
            <div class="c">Ofte stilte spørsmål</div>
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
    grid-template-areas:
    "a b c"
    "d e f"
    "g h i";
    padding-top: 65px;
    align-items: center;
}

.a, .d, .g{
    font-weight: 700px;
}

.d, .e, .f{
    font-weight: 700px;
}

.g, .h, .i{
    font-weight: 400px
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