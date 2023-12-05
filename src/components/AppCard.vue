<script>

export default {
    data() {
        return {
        }
    },
    props: {
        imageArray: Array,
    },
    methods: {
        getImagePath(image) {
            return new URL (`${image}`, import.meta.url).href;
        },
    }
}

</script>

<template>

<div v-for="image in imageArray" class="text-center">
    <img :src="getImagePath(image.img)" alt="food image">
    <h6 class="pt-3 pb-1 m-0">{{ image.txt }}</h6>
    <p class="pb-2 m-0">{{ image.by }}</p>
</div>
  
</template>

<style lang="scss" scoped>
@use "../style/partials/variables.scss" as *; 

h6 {
    color: $text-grey;
}
p {
    font-size: .7rem;
    color: $silver;
}
</style>