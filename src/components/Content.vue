<template>
    <section>
        <Jumbotron/>
        <div id="series">
            <Serie/>
        </div>
    </section>
</template>

<script>
import Jumbotron from './Jumbotron.vue';
import Serie from './Serie.vue';
export default {
    name: "ContentVue",
    components: { Jumbotron, Serie }
}
</script>

<style scoped lang="scss">
section {
    background-color: #1c1c1c;

    #series {
        width: 70%;
        margin: 0 auto;
        color: white;
    }
}
</style>