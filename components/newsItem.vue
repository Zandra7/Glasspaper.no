<template>
    <div class="container">
        <div class="news-container"> 
            <div>
                <img src="~/public/images/newsImage.png" alt="A group of people sitting on a bench">
            </div>
            <div class="text-container">
                <div><h4>{{ title1 }}</h4></div>
                <div><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sed libero facilisis, ullamcorper ex ac, ultricies diam. In consectetur venenatis ligula at ultrices. Nunc tincidunt quam at venenatis lacinia.</p></div>
            </div>
        </div>
        <div class="news-container"> 
            <div>
                <img src="~/public/images/newsImage.png" alt="A group of people sitting on a bench">
            </div>
            <div class="text-container">
                <div><h4>{{ title2 }}</h4></div>
                <div><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sed libero facilisis, ullamcorper ex ac, ultricies diam. In consectetur venenatis ligula at ultrices. Nunc tincidunt quam at venenatis lacinia.</p></div>
            </div>
        </div>
        <div class="news-container"> 
            <div>
                <img src="~/public/images/newsImage.png" alt="A group of people sitting on a bench">
            </div>
            <div class="text-container">
                <div><h4>{{ title3 }}</h4></div>
                <div><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sed libero facilisis, ullamcorper ex ac, ultricies diam. In consectetur venenatis ligula at ultrices. Nunc tincidunt quam at venenatis lacinia.</p></div>
            </div>
        </div>
    </div>
</template>

<script setup>
    const title1 = 'Nyhetssak 1'
    const title2 = 'Nyhetssak 2'
    const title3 = 'Nyhetssak 3'
</script>

<style scoped>
    .container {
        display: flex;
        flex-direction: row;
        align-items: center;
        max-width: 1170px;
        margin: 0 auto;
        justify-content: space-between;
    }

    .news-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 320px;
    }

    img {
        width: 320px;
    }

    .text-container {
        display: flex;
        flex-direction: column;
    }

    h4 {
        font-size: 18px;
    }

    p {
        font-size: 16px;
        font-weight: lighter;
    }
</style>