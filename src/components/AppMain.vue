<script>
import AppCard from './AppCard.vue';
export default {
    props: {
        social: Array,
    },
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
                {
                    img: "../assets/img/Mixed-fruits.jpg",
                    txt: "Food Corner: Top Japanese Restaurants for sushi",
                    flag: false
                },
                {
                    img: "../assets/img/r-rachel-park-366508-unsplash-min.jpg",
                    txt: "Roundup: My New Favourite Recipes For Healty Living",
                    flag: false
                },
                {
                    img: "../assets/img/r-michelle-tsang-500721-unsplash-min.jpg",
                    txt: "Why These Toast with Tea are My New Favourite",
                    flag: false
                },
                {
                    img: "../assets/img/r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg",
                    txt: "Food Corner: Top Japanese Restaurants for sushi",
                    flag: false
                },
                {
                    img: "../assets/img/fi-roundup.jpg",
                    txt: "Roundup: My New Favourite Recipes For Healty Living",
                    flag: false
                },
                {
                    img: "../assets/img/perfect-cosmopolitan-460x295.jpg",
                    txt: "Why These Toast with Tea are My New Favourite",
                    flag: false
                },
                {
                    img: "../assets/img/fi2x-6-460x295.jpg",
                    txt: "Food Corner: Top Japanese Restaurants for sushi",
                    flag: false
                },
                {
                    img: "../assets/img/r-brooke-lark-96398-unsplash-min-460x295.jpg",
                    txt: "Roundup: My New Favourite Recipes For Healty Living",
                    flag: false
                },
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
            ],
            postArray: [
                {
                    img: "../assets/img/single-post-img3.jpg",
                    txt: "Food Corner: Top Japanese Restaurants for sushi",
                    by: "March 25th, 2019"
                },
                {
                    img: "../assets/img/fi-korean-food.jpg",
                    txt: "Citu Guide: Singapore",
                    by: "February 27th, 2019"
                },
                {
                    img: "../assets/img/slide1-bg-150x150.jpg",
                    txt: "6 Nutritional Tips to Help Burn Body Fat",
                    by: "February 28th, 2019"
                },
            ],
            flagRecipe: false,
            flagPR: "popular",
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

    <div class=" my_container container-fluid pe-0 d-flex gap-5 pop-reci pb-5">
        <div class="row row_big">
            <div class="col">
                <div class="my_card">
                    <div class="position-relative" @mouseenter="flagRecipe = true" @mouseleave="flagRecipe = false">
                        <img src="../assets/img/Yogurt-Nan.jpg" alt="food image">
                        <div class="justify-content-center align-items-center text-center flex-column px-3 py-1" :class="flagRecipe ? 'd-flex over' : 'd-none'">
                            <div class="mb-4 rounded-circle d-flex justify-content-center align-items-center text-center"><i class="fa-solid fa-link"></i></div>
                            <h5>Lunch Favourite with Salad, Naan And Beans</h5>
                        </div>
                    </div>
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
            <div class="col" v-for="image in recipeImg">
                <div class="position-relative"  @mouseenter="image.flag = true" @mouseleave="image.flag = false">
                    <img :src="getImagePath(image.img)" alt="food image">
                    <div class="justify-content-center align-items-center text-center flex-column px-2 py-1" :class="image.flag ? 'd-flex over' : 'd-none'">
                        <div class="mb-1 rounded-circle d-flex justify-content-center align-items-center text-center"><i class="fa-solid fa-link"></i></div>
                        <h3>{{ image.txt }}</h3>
                    </div>
                </div>
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
            <div v-for="stamp in stamps" class="col text-center pb-2">
                <img class="" :src="getImagePath(stamp.img)" alt="stamps">
                <h6 class="m-0 p-2">{{ stamp.txt }}</h6>
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
            <div class="row g-0 gap-5">
                <div class="col-7">

                    <!-- big POST  SECTION -->
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

                    <!-- ADV SECTION -->
                    <div class="adv text-center pb-4">
                        <img src="../assets/img/ad-bg.jpg" alt="">
                        <h4 class="m-0">VIEW OUR LATEST RECIPES</h4>
                    </div>
                    <div class="city text-center">
                        <img src="../assets/img/singapore-featured-image.jpg" alt="">
                        <h4 class="guide p-3">City Guide: Singapore</h4>
                        <a class="orange-link p-2 d-block"><i class="fa-solid fa-earth-americas pe-2"></i>VIEW ALL CITY GIUDES</a>
                    </div>
                    <hr>

                    <!-- SEARCH -->
                    <div class="form-floating">
                        <input type="text" class="form-control" id="floatingInput" placeholder="name@example.com">
                        <label for="floatingInput"><i class="fa-solid fa-magnifying-glass pe-3"></i>Search</label>
                    </div>

                    <!-- SOCIAL LINKS SECTION -->
                    <h6 class="follow pt-4 pb-2">Follow Us</h6>
                    <div class="d-flex w-100 flex-wrap">
                        <div v-for="link in social" class="social me-2 d-flex justify-content-center align-items-center">
                            <a href="" :class="link"></a>
                        </div>
                        <div class="social me-2 d-flex justify-content-center align-items-center">
                            <a href="" class="fa-brands fa-pinterest-p"></a>
                        </div>
                    </div>

                    <!-- small POST SECTION -->
                    <div class="popular-recent mt-5">
                        <div class="d-flex text-center">
                            <h5 class="p-r_button" @click='flagPR="popular"' :class='flagPR === "popular" ? "active" : ""'>Popular</h5>
                            <h5 class="p-r_button" @click='flagPR="recent"' :class='flagPR === "recent" ? "active" : ""'>Recent</h5>
                        </div>    
                        <div v-for="post in postArray" class="d-flex align-items-center pt-4">
                            <img :src="getImagePath(post.img)" alt="" class="rounded-circle">
                            <div class="ps-3">
                                <h6 class="m-0">{{ post.txt }}</h6>
                                <p class="m-0">{{ post.by }}</p>
                            </div>
                        </div>
                    </div>

                    <!-- TWEET SECTION -->
                    <div class="tweet p-3 mt-5 rounded-3">
                        <div class="tweet-top d-flex justify-content-between align-items-center">
                            <div>
                                <h4 class="d-inline-block m-0 pe-2">Tweets</h4>
                                <a href="">by @Theme_Fusion</a>
                            </div>
                            <i class="fa-solid fa-circle-info"></i>
                        </div>
                        <div class="d-flex pt-3">
                            <img class="tweet-logo me-2" src="../assets/img/3a74ce3d0532b7773b174c45ca3bd05a_normal.png" alt="">
                            <div class="tweet-body">
                                <div class="d-flex justify-content-between">
                                    <div>
                                        <h6 class="m-0">ThemeFusion</h6>
                                        <p class="tag m-0">@Theme_Fusion</p>
                                    </div>
                                    <i class="fa-brands fa-twitter"></i>
                                </div>
                                <p class="text m-0">Do you need sublime WorldPress hosting for your next website? Take advantige of exclusive partners offers that we have secured just for you &lounch your site in seconds with <a href="">#avada</a> on WP Engine hosting & get 30% Off this Black Friday</p>
                                <a href="">bit.ly/3kjLLe2#BlackFriday2020</a>
                                <img class="pb-2 pt-4" src="../assets/img/En2TRxLW4AEiWUN.jpeg" alt="tweet image">
                                <div class="d-flex justify-content-between">
                                    <div>
                                        <i class="pe-3 fa-regular fa-heart"></i>
                                        <i class="fa-solid fa-right-from-bracket"></i>
                                    </div>
                                    <p class="hour">21<a class="h" href="">h</a></p>
                                </div>
                            </div>
                        </div>
                    </div>
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
    .pop-reci {
        .row_big {
            width: 100%;
            .col {
                width: 100%;
                padding: 0;
                .my_card {
                    background-color: white;
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
                        h5 {
                            font-size: 1.3rem;
                            color: white;
                        }
                    }
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
                .over {
                    position: absolute;
                    height:100%;
                    width:100%;
                    top:0;
                    left:0;
                    background-image: linear-gradient(rgba(252, 117, 37, 0.6), $orange);
                    div {
                        width: 30px;
                        height: 30px;
                        color: black;
                        background-color: white;
                    }
                    h3 {
                        font-size: .7rem;
                        color: white;
                    }
                }
            }
        }
        
    }

    // CULINARY SCETION
    .culinary {
        .row {
            gap: 40px;
            .col {
                width: calc((100% / 4) - 30px);
                background-color: white;
                img {
                    height: 80px;
                }
                h6 {
                    font-size: .8rem;
                    
                }
                &:hover {
                    h6 {
                        background-color: $orange;
                        color: white;
                    }
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
            .col-7 {
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
                        width: 35%;
                        position: absolute;
                        left: 50%;
                        top: 48%;
                        transform: translate(-50%, -50%);
                        font-size: 120%;
                        letter-spacing: 2px;
                        line-height: 2rem;
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
                .form-floating {
                    font-size: .9rem;
                    color: $silver;
                }
                .follow {
                    color: $orange;
                }
                .social {
                    width: 40px;
                    aspect-ratio: 1 / 1;
                    background-color: $wood-white-dark;
                    border: .5px solid $silver;
                    border-radius: 3px;
                    a {
                        scale: 1.3;
                        color: $text-grey;
                    }
                }
                .popular-recent {
                    .p-r_button {
                        width: calc(100% / 2);
                        padding: 15px;
                        border: .5px solid $silver;
                        font-size: 1rem;
                        &.active {
                            background-color: white;
                        }
                    }
                    .rounded-circle {
                        width: 55px;
                        height: 55px;
                    }
                    h6 {
                        line-height: 2rem;
                        color: $text-grey;
                    }
                    p {
                        padding-top: 5px;
                        font-size: .9rem;
                        color: $silver;
                    }
                }
                .tweet {
                    background-color: white;
                    width: 100%;
                    h4 {
                        color: $text-grey;
                    }
                    a {
                        color: $blue;
                        font-size: .8rem;
                    }
                    .tweet-logo {
                        width: 30px;
                        height: 30px;
                    }
                    .tweet-body {
                        width: 85%;
                        word-wrap: break-word;
                        .tag {
                            color: $silver;
                        }
                        i {
                            color: $silver;
                        }
                        .hour {
                            color: $silver;
                        }
                        .text {
                            font-size: .9rem;
                            color: $text-grey;
                        }
                    }
                }
            }
        }
    }
}
</style>