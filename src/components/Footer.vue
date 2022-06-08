<template>
    <footer>
        <FooterUp/>
        <FooterDown/>
    </footer>
</template>

<script>
import FooterUp from './FooterUp.vue';
import FooterDown from './FooterDown.vue';
export default {
    name: "FooterVue",
    components: { FooterUp, FooterDown }
}
</script>

<style scoped lang="scss">

</style>