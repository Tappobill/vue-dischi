<template>
<div class="col">
    <div class="card">
        <img :src="primaProps.poster" class="card-img-top" alt="...">
        <div class="card-body">
            <div class="text-center">
                <h5 class="card-title text-uppercase">{{ primaProps.title }}</h5>
                <div>{{ primaProps.author }}</div>
                <div>{{ primaProps.year }}</div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: "AlbumCard",
    props: {
        primaProps: Object
    }
}
</script>

<style lang="scss" scoped>
.card {
    background-color: #2e3a46;
    height: 400px;
    margin-top: 20px;
}
</style>