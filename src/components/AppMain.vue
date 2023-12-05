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
            recipeImg: [
                "../assets/img/Mixed-fruits.jpg",
                "../assets/img/r-rachel-park-366508-unsplash-min.jpg",
                "../assets/img/r-michelle-tsang-500721-unsplash-min.jpg",
                "../assets/img/quick-summer-drink-460x295.jpg",
                "../assets/img/r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg",
                "../assets/img/perfect-cosmopolitan-460x295.jpg",
                "../assets/img/fi2x-6-460x295.jpg",
                "../assets/img/r-brooke-lark-96398-unsplash-min-460x295.jpg",
            ],
            stamps: [
                {
                    img: "../assets/img/drinks-recipes.png",
                    txt: "DRINKS"
                },
                {
                    img: "../assets/img/soups-recipes.png",
                    txt: "SOUPS"
                },
                {
                    img: "../assets/img/baking-recipes.png",
                    txt: "BAKERY"
                },
                {
                    img: "../assets/img/dinner-recipes.png",
                    txt: "DINNER"
                },
                {
                    img: "../assets/img/healthy-recipes.png",
                    txt: "HEALTY"
                },
                {
                    img: "../assets/img/staff-picks.png",
                    txt: "STAFF PICKS"
                },
                {
                    img: "../assets/img/premium-recipes.png",
                    txt: "APPETISER"
                },
                {
                    img: "../assets/img/quick-easy-recipes.png",
                    txt: "QUICK & EASY"
                },
            ],
            imagesFarm: [
                {
                    img: "../assets/img/fi-roundup.jpg",
                    txt: "Roundup: My New Favourite Recipes For Healty Living",
                    by: "By admin | March 25th, 2019"
                },
                {
                    img: "../assets/img/fi-korean-food.jpg",
                    txt: "Meal Prep: Korean Bibimbap with Kimchi",
                    by: "By admin | March 25th, 2019"
                },
                {
                    img: "../assets/img/fi-toasts.jpg",
                    txt: "Why These Toast with Tea are My New Favourite",
                    by: "By admin | March 25th, 2019"
                },
                {
                    img: "../assets/img/fi-street-food.jpg",
                    txt: "Exploring Streat Food in Bangkok",
                    by: "By admin | March 25th, 2019"
                },
                {
                    img: "../assets/img/fi-organic-breakfast.jpg",
                    txt: "Oranic Choices For Healtier Living",
                    by: "By admin | March 25th, 2019"
                },
                {
                    img: "../assets/img/fi-water-side-rest.jpg",
                    txt: "5 Waterslide Restaurant in Instanbul fo Special Events",
                    by: "By admin | March 25th, 2019"
                },
            ]
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
            <div v-for="image in foodieImg" class="text-center">
                <AppCard :image="image"/>
            </div>
        </div>
    </div>
    
    <!-- POPULAR RECIPE SECTION -->
    <div class="small_container text-center pb-5">
        <h4 class="py-3">POPULAR RECIPES</h4>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, minima culpa!</p>
    </div>

    <div class=" my_container container-fluid pe-0 d-flex gap-5 pop-rec pb-5">
        <div class="row row_big">
            <div class="col">
                <div class="my_card">
                    <img src="../assets/img/Yogurt-Nan.jpg" alt="food image">
                    <div class="p-4">
                        <h5 class="m-0 py-1">Lunch Favourite with Salad, Naan And Beans</h5>
                        <p>Bakery, Featured, Healty, Latest Recipes, Staff Picks</p>
                        <hr>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas, itaque cupiditate repudiandae necessitatibus amet cumque ipsam magnam, laborum fugiat, quaerat pariatur consequuntur quisquam totam. Quo accusamus dicta iusto cupiditate deserunt! Amet et voluptatibus commodi accusamus fugiat nobis? Earum neque sequi aliquid iste voluptate? Eveniet iure cupiditate nostrum quod unde officiis porro id rerum illo libero. Officiis cumque a suscipit tempore?</p>
                        <a class="my_btn" href="">LEARN MORE</a>
                    </div>
                </div>
            </div>
        </div>
        <div class="row row-cols-2 row-gap-3">
            <div v-for="image in recipeImg" class="col">
                <img :src="getImagePath(image)" alt="food image">
            </div>
        </div>
    </div>

    <!-- CULINARY COLLECTION SECTION -->
    <div class="small_container text-center pb-4 pt-5">
        <h4 class="py-3">CULINARY COLLECTION</h4>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, minima culpa!</p>
    </div>

    <div class="my_container container-fluid culinary pb-5">
        <div class="row row-cols-4">
            <div v-for="stamp in stamps" class="col text-center">
                <img :src="getImagePath(stamp.img)" alt="stamps">
                <h6>{{ stamp.txt }}</h6>
            </div>
        </div>

    </div>

    <!-- FARM TO TABLE SECTION -->
    <div class="farm pb-5">
        <div class="my_container py-5">
            <div class="d-flex justify-content-between align-items-start">
                <div class="small_container_farm m-0">
                    <h4 class="py-3 m-0">FARM TO TABLE</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, minima culpa!</p>
                </div>
                <a class="my_btn" href="">READ OUR BLOG<i class="fa-solid fa-book-open-reader ps-2"></i></a>
            </div>
        </div>    
        <div class=" my_container container-fluid p-0">
            <div class="row g-0 gap-4">
                <div class="col-8">
                    <div class="my_card mb-3">
                        <img src="../assets/img/single-post-img3.jpg" alt="food image">
                        <div class="p-4">
                            <h5 class="m-0 py-1">Food Corner: Top Japanese Restaurants for Sushi</h5>
                            <p>By admin | March 25th, 2019</p>
                            <hr>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas, itaque cupiditate repudiandae necessitatibus amet cumque ipsam magnam, laborum fugiat, quaerat pariatur consequuntur quisquam totam. Quo accusamus dicta iusto cupiditate deserunt! Amet et voluptatibus commodi accusamus fugiat nobis? Earum neque sequi aliquid iste voluptate? Eveniet iure cupiditate nostrum quod unde officiis porro id rerum illo libero. Officiis cumque a suscipit tempore?</p>
                            <div class="d-flex justify-content-between">
                                <a class="my_link" href="">Read More ></a>
                                <button class="border-0"><i class="fa-regular fa-comments"></i>0</button>
                            </div>
                        </div>
                    </div>
                    <div class="line d-flex flex-wrap justify-content-between">
                        <div v-for="image in imagesFarm" class="colum d-flex my-3">
                            <div class="my_card text-center">
                                <AppCard :image="image"/>
                            </div>
                        </div>
                    </div>
                    <div class="grey-button">
                        <h4 class="text-center py-3">LOAD MORE POSTS</h4>
                    </div>
                </div>
                <div class="col">
                    <div class="adv text-center pb-4">
                        <img src="../assets/img/ad-bg.jpg" alt="">
                        <h4>VIEW OUR LATEST RECIPES</h4>
                    </div>
                    <div class="city text-center">
                        <img src="../assets/img/singapore-featured-image.jpg" alt="">
                        <h4 class="guide p-2">City Guide: Singapore</h4>
                        <a class="orange-link p-2 d-block"><i class="fa-solid fa-earth-americas pe-2"></i>VIEW ALL CITY GIUDES</a>
                    </div>
                    <hr>
                </div>
            </div>
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
            opacity: 0.4;
            color: $silver;
        }
    }
    .small_container {
        width: 30%;
        margin: 0 auto;
        h4 {
            color: $text-grey;
            font-size: 1.1rem;
            letter-spacing: 1px;
        }
        p {
            color: $text-grey;
            font-size: .8rem;
        }
    }

    // POPULAR RECIPE
    .pop-rec {
        .row_big {
            width: 100%;
            .col {
                width: 100%;
                padding: 0;
                .my_card {
                    background-color: white;
                    h5 {
                        font-size: 1.1rem;
                        color: $text-grey;
                    }
                    p {
                        font-size: .8rem;
                        color: $silver;
                        line-height: 1.4rem;
                    }
                    hr {
                        opacity: .4;
                        color: $silver;
                    }
                    .my_btn {
                        background-color: $orange;
                        color: white;
                        font-size: .8rem;
                        padding: 10px 20px;
                    }
                }
            }
        }
        .row-cols-2 {
            width: 100%;
            .col {
                width: calc(100% / 2);
            }
        }
        
    }

    // CULINARY SCETION
    .culinary {
        .row {
            gap: 40px;
            .col {
                padding: 10px 50px;
                width: calc((100% / 4) - 30px);
                background-color: white;
                h6 {
                    font-size: .7rem;
                }
            }
        }
    }

    // FARM TO TABLE SECTION
    .farm {
        .small_container_farm {
            width: 50%;
            h4 {
                color: $text-grey;
                font-size: 1.1rem;
                letter-spacing: 1px;
            }
            p {
                color: $text-grey;
                font-size: .8rem;
            }
            
        }
        .my_btn {
            background-color: $orange;
            color: white;
            font-size: .8rem;
            padding: 10px 20px;
        }
        .row {
            width: 100%;
            .col-8 {
                .my_card {
                    background-color: white;
                    h5 {
                        font-size: 1.1rem;
                        color: $text-grey;
                    }
                    p {
                        font-size: .8rem;
                        color: $silver;
                        line-height: 1.4rem;
                    }
                    hr {
                        opacity: .4;
                        color: $silver;
                    }
                    a {
                        font-size: .7rem;
                        color: $silver;
                    }
                    button {
                        background-color: white;
                        font-size: .8rem;
                        color: $silver;
                    }
                }
                .line {
                    width: 100%;
                    .colum {
                        width: calc((100% / 2) - 20px);
                    }
                }
                .grey-button {
                    background-color: $wood-white-dark;
                    
                    h4 {
                        color: $text-grey;
                        font-size: 1.1rem;
                    }
                }
            }
            .col {
                .adv {
                    position: relative;
                    h4 {
                        width: 40%;
                        position: absolute;
                        left: 50%;
                        top: 50%;
                        transform: translate(-50%, -50%);
                        font-size: 1rem;
                        letter-spacing: 2px;
                    }
                }
                .city {
                    position: relative;
                    .orange-link {
                        background-color: $orange;
                        color: white;
                        font-size: .9rem;
                    }
                    .guide {
                        background-color: black;
                        color: white;
                        opacity: .8;
                        font-size: 1.1rem;
                        position: absolute;
                        top: 50%;
                        left: 0;
                    }
                }
                hr {
                    color: $silver;
                    opacity: .4;
                }
            }
        }
    }
}
</style>