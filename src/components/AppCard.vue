<script>

export default {
    data() {
        return {
            flag: false,
        }
    },
    props: {
        image: Object,
    },
    methods: {
        getImagePath(image) {
            return new URL (`${image}`, import.meta.url).href;
        },
    }
}

</script>

<template>

    <div class="over-action" @mouseenter="flag = true" @mouseleave="flag = false">
        <div class="position-relative">
            <img :src="getImagePath(image.img)" alt="food image">
            <div class="justify-content-center align-items-center text-center flex-column px-3 py-1" :class="flag ? 'd-flex over' : 'd-none'">
                <div class="mb-2 rounded-circle d-flex justify-content-center align-items-center text-center"><i class="fa-solid fa-link"></i></div>
                <h3>{{ image.txt }}</h3>
            </div>
        </div>
        <h6 class="pt-3 px-3 pb-1 m-0">{{ image.txt }}</h6>
        <p class="pb-3 m-0">{{ image.by }}</p>
    </div> 
</template>

<style lang="scss" scoped>
@use "../style/partials/variables.scss" as *; 

.over-action {
    .over {
        position: absolute;
        height:100%;
        width:100%;
        top:0;
        left:0;
        background-image: linear-gradient(rgba(252, 117, 37, 0.6), $orange);
        div {
            width: 40px;
            height: 40px;
            color: black;
            background-color: white;
        }
        h3 {
            font-size: 1rem;
            color: white;
        }
    }
}
h6 {
    color: $text-grey;
}
p {
    font-size: .7rem;
    color: $silver;
}
</style>