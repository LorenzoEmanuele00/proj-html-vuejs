<script>
import AppCard from './AppCard.vue';
export default {
    components: {
        AppCard,
    },
    data() {
        return {
            foodieImg: [
                {
                    img: "../assets/img/single-post-img3.jpg",
                    txt: "Food Corner: Top Japanese Restaurants for sushi",
                    by: "By admin | March 25th, 2019"
                },
                {
                    img: "../assets/img/fi-roundup.jpg",
                    txt: "Roundup: My New Favourite Recipes For Healty Living",
                    by: "By admin | March 25th, 2019"
                },
                {
                    img: "../assets/img/fi-toasts.jpg",
                    txt: "Why These Toast with Tea are My New Favourite",
                    by: "By admin | March 25th, 2019"
                }
            ],
        }
    },
    methods: {
        getImagePath(image) {
            return new URL (`${image}`, import.meta.url).href;
        },
    }
}
</script>

<template>

<!-- HERO SECTION -->
<div class="hero d-flex justify-content-center align-items-center flex-column">
    <div class="hero-text text-center rounded-3 mb-3">
        <h2 class="pt-5">Food Corner: Top Japanese Restaurants for sushi</h2>
        <p class="pt-2">March 25, 2019</p>
    </div>
    <div class="orange-top py-2 px-4 rounded-3">TODAY'S PICK</div>
</div>

<!-- MAIN SECTION -->
<div class="bg-b">

    <!-- FOODIE JOURNAL SECTION -->
    <div class="my_container foodie py-3 ">
        <div class="d-flex justify-content-center align-items-center pb-3">
            <hr>
            <h5 class="my-0 px-5">FOODIE JOURNAL</h5>
            <hr>
        </div>
        <div class="d-flex justify-content-center align-items-center gap-4 px-4">
            <AppCard :imageArray="foodieImg"/>
        </div>
    </div>
</div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables.scss" as *; 

// HERO SECTION
.hero {
    background-image: url('../assets/img/single-post-img3.jpg');
    background-position: center;
    background-size: 100%;
    min-height: 500px;
    .hero-text {
        background-color: white;
        width: 500px;
        height: 200px;
        p {
            color: $text-grey;
        }
    }
    .orange-top {
        background-color: $orange;
        color: white;
        font-size: .9rem;
        font-weight: bold;
        position: relative;
        top: -235px;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.08), 0 4px 8px 0 rgba(0, 0, 0, 0.08);
    }
}

// MAIN SECTION
.bg-b{
    background-color: $wood-white;

// FOODIE JOURNAL SECTION
    .foodie {
        background-color: white;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.08), 0 4px 8px 0 rgba(0, 0, 0, 0.08);
        position: relative;
        top: -70px;
        h5 {
            color: $text-grey;
            font-size: 1rem;
        }
        hr {
            width: 34%;
            border: .5px solid;
            opacity: .8;
            color: $silver;
        }
    }
}
</style>