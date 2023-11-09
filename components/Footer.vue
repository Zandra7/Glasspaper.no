<template>
<div class="background">
        <div class="container">
            <div class="a">Glasspaper deler</div>
            <div class="b">Konsernledelse</div>
            <div class="c">Privacy and Cookie Policy</div>
            <div class="d">Ofte stilte spørsmål</div>
            <div class="e">Våre lokasjoner</div>
            <div class="f">Legal Terms of Service</div>
            <div class="g">Våre selskaper</div>
            <div class="h"><img src="~/public/images/icons.png"></div>
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

img{
    width: 213px;
    height: 52px;
}

@media(max-width:1175px){
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
    margin-left: 10px;
    margin-right: 10px;
    max-width: 1170px;
    }
}

@media(max-width: 620px){
    .container{
    color: white;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-areas:
    "a"
    "d"
    "g"
    "b"
    "e"
    "i"
    "c"
    "f"
    "h";
    padding-top: 65px;
    padding-bottom: 77px;
    margin-top: 83px;
    margin-left: 10px;
    margin-right: auto;
    max-width: 1170px;
    }

    .a{
    font-weight: 700;
    padding-top: 35px;
    grid-area: a; 
    }
    .b{
    font-weight: 700;
    padding-top: 35px;
    grid-area: b; 
    }
    .c{
    font-weight: 400;
    padding-top: 35px;
    grid-area: c; 
    }
    .d{
    font-weight: 700;
    padding-top: 35px;
    grid-area: d; 
    }
    .e{
    font-weight: 700;
    padding-top: 35px;
    grid-area: e; 
    }
    .f{
    font-weight: 400;
    padding-top: 35px;
    grid-area: f; 
    }
    .g{
    font-weight: 700;
    padding-top: 35px;
    grid-area: g; 
    }
    .h{
    font-weight: 700;
    padding-top: 35px;
    grid-area: h; 
    }
    .i{
    font-weight: 400;
    padding-top: 35px;
    grid-area: i; 
    }
    
}

</style>