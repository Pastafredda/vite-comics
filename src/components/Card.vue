<script>
export default {
    name: "Card",
    props: {
        details: Object
    }

}
</script>

<template>
    <div class="comic">
        <img :src="details.thumb" alt="details.series">
        <h5>{{ details.series }}</h5>
    </div>
</template>

<style lang="scss" scoped>
.comic {
    width: calc(100% / 6);
    padding: 20px;
}

h5 {
    color: white;
}
</style>