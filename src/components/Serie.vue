<template>
    <div class="card-serie">
        <img :src="serie.thumb" alt="serie.series">
        <span>{{serie.series}}</span>
    </div>
</template>

<script>
export default {
    name: 'SerieVue',
    props : {
        serie: Object
  }
}
</script>

<style scoped lang="scss">
.card-serie {
    width: calc(100% / 6);
    padding: 12px;
    margin-top: 30px;

    img {
        width: 100%;
        max-height: 200px;
        object-fit: cover;
        object-position: top;
        margin-bottom: 10px;
    }
}
</style>