<template>
    <main>
        <div class="container">
            <AlbumList />
        </div>
    </main>
</template>

<script>
import AlbumList from "./albums/AlbumList.vue"
export default {
    name: 'MainComp',
    components: {
        AlbumList
    }
}
</script>
    
<style lang="scss" scoped>
main {
    height: 90%;
    background-color: #1e2d3b;
    color: white;
}
</style>