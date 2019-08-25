<template>
    <div>
        <img v-for="image in allImages" :src="image.link" :key="image.link" />
    </div>
</template>

<script>
import { mapActions, mapGetters } from 'vuex'

export default {
    name: 'image-list',
    methods : mapActions (['fetchImages']),
    computed: mapGetters (['allImages']),
    created(){
        this.fetchImages()
    }
}
</script>

<style>

</style>
