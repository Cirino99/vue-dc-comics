<template>
    <section>
        <div>
            <div>
                <a href="#">SIGN-UP NOW!</a>
            </div>
            <div id="footer-follow">
                <span>FOLLOW US</span>
                <img v-for="(follow,index) in follows" :key="index" :src="follow" alt="">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "FooterDownVue",
    data(){
        return {
            follows : [require('../assets/img/footer-facebook.png'),require('../assets/img/footer-twitter.png'),require('../assets/img/footer-youtube.png'),require('../assets/img/footer-pinterest.png'),require('../assets/img/footer-periscope.png')]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/vars";
section {
    background-color: #303030;

    div {
        width: 70%;
        margin: 0 auto;
        padding: 20px 0;
        display: flex;
        justify-content: space-between;

        div {
            display: flex;
            align-items: center;
            justify-content: space-between;

            a {
                display: block;
                padding: 12px;
                border: 2px solid $primary;
                color: white;
                font-weight: 600;
                text-decoration: none;
            }

            &#footer-follow {
                width: 430px;

                span {
                    color: $primary;
                    font-weight: 600;
                    font-size: 18px;
                }
            }
        }
    }
}
</style>