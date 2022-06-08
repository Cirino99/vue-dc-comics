<template>
    <section>
        <div>
            <div id="footer-links">
                <div>
                    <h3>{{list[0].text}}</h3>
                    <ul>
                        <li v-for="(link,index) in list[0].links" :key="index">
                            <a href="#">{{link}}</a>
                        </li>
                    </ul>
                    <h3>{{list[1].text}}</h3>
                    <ul>
                        <li v-for="(link,index) in list[1].links" :key="index">
                            <a href="#">{{link}}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3>{{list[2].text}}</h3>
                    <ul>
                        <li v-for="(link,index) in list[2].links" :key="index">
                            <a href="#">{{link}}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3>{{list[3].text}}</h3>
                    <ul>
                        <li v-for="(link,index) in list[3].links" :key="index">
                            <a href="#">{{link}}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div id="footer-logo">

            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "FooterUpVue",
    data(){
        return {
            list: [
                {
                    text: 'DC COMICS',
                    links : ['Characters','Comics','Movies','TV','Games','Videos','News']
                },
                {
                    text: 'SHOP',
                    links : ['Shop DC','Shop DC Collectibles']
                },
                {
                    text: 'DC',
                    links : ['Term Of Use','Privacy Policy','Ad Choices','Advertising','Jobs','Subscriptions','Talent Workshops','CPSC Certificates','Ratings','Shop Help','Contact Us']
                },
                {
                    text: 'SITES',
                    links : ['DC','MAD Magazine','DC Kids','DC Universe','DC Powe Visa']
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
section {
    background-image: url('../assets/img/footer-bg.jpg');
    height: 360px;
    div {
        height: 100%;
        width: 70%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;

        #footer-links {
            padding: 20px 0;
            display: flex;
            width: 40%;
            margin: 0;

            div {
                display: flex;
                flex-direction: column;
                justify-content: flex-start;

                h3 {
                    color: white;
                    margin: 20px 0;
                }

                ul {
                    li {
                        list-style-type: none;

                        a {
                            color: #959595;
                            font-size: 14px;
                            text-decoration: none;
                        }
                    }
                }
            }
        }

        #footer-logo {
            background-image: url('../assets/img/dc-logo-bg.png');
            background-repeat: no-repeat;
            background-position: center;
            width: 50%;
            margin: 0;
        }
    }
}
</style>