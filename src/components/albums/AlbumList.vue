<template>
    <div id="albumsList" class="row row-cols-5 justify-content-between">
        <AlbumCard v-for="(elem, index) in albums" :key="index" :primaProps="elem" />
    </div>
</template>

<script>
import AlbumCard from "./AlbumCard.vue"
import axios from "axios";

export default {
    name: "AlbumList",
    components: {
        AlbumCard
    },
    data() {
        return {
            albums: []
        }
    },
    mounted() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((response) => {
                this.albums = response.data.response
            })
    }
}
</script>

<style lang="scss" scoped>
#albumsList {}
</style>