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
            albums: [],
            arrayGeneriMain: [],
            arrayAutoriMain: []
        }
    },
    mounted() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((response) => {
                this.albums = response.data.response

                this.albums.forEach((singleAlbum) => {

                    if (!this.arrayGeneriMain.includes(singleAlbum.genre)) {
                        this.arrayGeneriMain.push(singleAlbum.genre)
                    }
                    this.arrayAutoriMain.push(singleAlbum.author)
                    
                    this.$emit('emitGeneriMain', this.arrayGeneriMain)
                    this.$emit('emitAutoriMain', this.arrayAutoriMain)


                })
            })
    }
}
</script>

<style lang="scss" scoped>

</style>