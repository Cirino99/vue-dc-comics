<template>
    <section>
        <div>
            <div v-for="(material,index) in shopMaterials" :key="index">
                <img :src="material.img" :alt="material.text">
                <span>{{material.text}}</span>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'ContentShopVue',
    data(){
        return {
            shopMaterials: [
                {
                    img: require('../assets/img/buy-comics-digital-comics.png'),
                    text: 'DIGITAL COMICS'
                },
                {
                    img: require('../assets/img/buy-comics-merchandise.png'),
                    text: 'DC MERCHANDISE'
                },
                {
                    img: require('../assets/img/buy-comics-subscriptions.png'),
                    text: 'SUBSCRIPTION'
                },
                {
                    img: require('../assets/img/buy-comics-shop-locator.png'),
                    text: 'COMIC SHOP LOCATOR'
                },
                {
                    img: require('../assets/img/buy-dc-power-visa.svg'),
                    text: 'DC POWER VISA'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/vars";
section {
    background-color: $primary;
    padding: 40px 0;

    div {
        width: 70%;
        margin: 0 auto;
        display: flex;
        padding: 0 25px;

        div {
            display: flex;
            align-items: center;
            gap: 25px;

            img {
                max-width: 50px;
                height: auto;
                max-height: 60px;
            }

            span {
                color: white;
                font-size: 15px;
                font-weight: 400;
            }
        }
    }
}
</style>