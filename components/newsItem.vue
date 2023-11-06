<template>
    <h2>Aktuelle Saker</h2>
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
    h2 {
        display: flex;
        padding: 1.5rem 0;
        font-size: 32px;
        max-width: 1170px;
        margin: 0 auto;
    }
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
    @media (max-width: 1175px) {
        .container, h2 {
            padding: 0 2rem;
        }
    }

    @media (max-width: 1050px) {
        h2 {
            font-size: 26px;
            padding-bottom: 1.5rem;
        }

        .container {
            flex-direction: column;
            align-items: flex-start;
        }

        .news-container {
            flex-direction: row;
            width: 100%;
            justify-content: space-between;
            padding-bottom: 1rem;
        }

        img {
            width: 100%;
            max-width: 320px;
            height: auto;
            min-width: 200px;
        }

        h4, p{
            padding-left: 0.5rem;
        }

        @media (max-width: 620px) {
            h2 {
                font-size: 22px;
            }

            h4, p {
                padding-left: 0;
            }
            .container {
                flex-direction: column;
            }

            .news-container {
                flex-direction: column;
                width: 100%;
            }

            p {
                display: none;
            }
        }
    }
</style>