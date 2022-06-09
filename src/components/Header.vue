<template>
    <header>
        <nav>
            <img :src="logo" alt="">
            <ul>
                <li v-for="(link,index) in links" :key="index">
                    <a :class="link.current ? 'active' : ''" :href="link.url">
                        {{link.text}}
                        <div v-if="link.current"></div>
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'HeaderVue',
    data(){
        return {
            logo: require('../assets/img/dc-logo.png'),
            links: [
                {
                    text: 'CHARACTERS',
                    url: '#',
                    current: false
                },
                {
                    text: 'COMICS',
                    url: '#',
                    current: true
                },
                {
                    text: 'MOVIES',
                    url: '#',
                    current: false
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false
                },
                {
                    text: 'GAMES',
                    url: '#',
                    current: false
                },
                {
                    text: 'COLLECTIBLES',
                    url: '#',
                    current: false
                },
                {
                    text: 'VIDEOS',
                    url: '#',
                    current: false
                },
                {
                    text: 'FANS',
                    url: '#',
                    current: false
                },
                {
                    text: 'NEWS',
                    url: '#',
                    current: false
                },
                {
                    text: 'SHOP',
                    url: '#',
                    current: false
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/vars";
header {
    height: 120px;
    display: flex;
    align-items: center;
    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 70%;
        height: 100%;
        margin: 0 auto;
        
        ul {
            list-style-type: none;

            li {
                display: inline-block;
                margin: 0 10px;

                a {
                    text-decoration: none;
                    color: #464646;
                    position: relative;
                    font-weight: 600;

                    &.active {
                        color: $primary;
                    }

                    div {
                        position: absolute;
                        height: 5px;
                        width: 100%;
                        bottom: -51px;
                        left: 0;
                        background-color: $primary;
                    }
                }
            }
        }
    }
}
</style>