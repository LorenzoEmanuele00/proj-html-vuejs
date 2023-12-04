<script>
export default {
    props: {
        menu: Array,
        social: Array,
    },
    data() {
        return {    
            stripImages: [
                "../assets/img/Yogurt-Nan.jpg",
                "../assets/img/Mixed-fruits.jpg",
                "../assets/img/r-rachel-park-366508-unsplash-min.jpg",
                "../assets/img/r-michelle-tsang-500721-unsplash-min.jpg",
            ]
        }
    },
    methods: {
        getImagePath(image) {
            return new URL (`${image}`, import.meta.url).href;
        },
    }
};
</script>

<template>

    <!-- SUBSCRIBE SECTION -->
<section class="upper d-flex justify-content-center align-items-center">
    <div class="small-container text-center">
        <h2>Subscribe <span class="orange">&</span> Receive A Free eBook</h2>
        <p class="text-color">Lorem ipsum dolor lorem lorem lorem lorem sit amet consectetur adipisicing elit. Dolorem harum dicta minus iusto.</p>
        <div class="text-color d-flex justify-content-between my-4">
            <div class="form-floating w-100">
                <input type="email" class="form-control border-2" id="floatingInput" placeholder="name@example.com">
                <label for="floatingInput">Insert your email ...*</label>
            </div>
            <button class="my_btn ms-3">SUBSCRIBE</button> 
        </div>   
        <p class="text-color p-minor">Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
    </div>
</section>

<!-- IMAGE STRIP SECTION -->
<section class="middle d-flex align-items-start">
    <img v-for="image in stripImages" :src="getImagePath(image)" alt="food image" class="img-dim mt-4">
</section>

<!-- BOTTOM SQUARES SECTION -->
<section id="info" class="bottom my_container d-flex">

    <!-- LOGO AND SOCIALS -->
    <div class="square bord">
        <img src="../assets/img/avada-food-logo-mob-2x.png" alt="avada food logo" class="foot-logo">
        <a v-for="link in social" href="" :class="link" class="ps-3 socials"></a>
    </div>

    <!-- MENU -->
    <div class="square bord">
        <a v-for="link in menu" href="" class="d-block menu">{{ link !== "Home" ? link : '' }}</a>
    </div>

    <!-- CONTACTS -->
    <div class="square bord">
        <h6 class="mb-4">CONTACT</h6>
        <p><i class="fa-solid fa-location-dot mt-1"></i> 775 New York Ave, Broklyn, Kings, New York 11203</p>
        <p><i class="fa-solid fa-phone mt-1"></i>+0100-505-0000</p>
        <p><i class="fa-solid fa-envelope mt-1"></i>info@your-domain.com</p>
    </div>

    <!-- DOWNLOAD -->
    <div class="square">
        <h6 class="mb-4">GET YOUR APP</h6>
        <img class="mb-3" src="../assets/img/download-android.png" alt="download android">
        <img src="../assets/img/download-app-store.png" alt="download app store">
    </div>
</section>

<section class="last position-relative py-4">
    <a href="#top-page" class="rounded-circle">^</a>
    <p class="m-0">Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Right Reserved | Powered by WorldPress</p>
</section>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables.scss" as *; 
.upper {
    background-image: url('../assets/img/subscribe-sec-bg.png');
    background-position: 50%;
    background-size: 120%;
    padding: 20px 0;
}
.small-container {
    width: 43%;
    margin: 0 auto;
    .text-color {
        color: $text-grey;
    }
    h2 {
        font-size: 1.6rem;
        padding-bottom: 10px;
        .orange {
            color: $orange;
        }
    }
    p {
        font-size: .9rem;
    }
    .form-floating {
        color: $silver;
    }
    .p-minor {
        font-size: .8rem;
    }
    .my_btn {
        border: 0;
        padding: 0 50px;
        background-color: $orange;
        color: white;
    }
}

// IMAGE STRIP SCETION
.middle {
    background-image: url('../assets/img/subscribe-sec-bg.png');
    background-position-x: 50%;
    background-position-y: bottom;
    background-size: 120%;
    img {
        width: calc(100% / 4);
    }
}

// BOTTOM SQUARE SECTION
.my_container {
    .square {
        margin-top: 50px;
        width: calc(100% / 4);
        padding: 10px 25px 0 25px;
        &.bord {
            border-right: 1px dashed $silver;
        }
        p {
            color: $text-grey;
            display: flex;
            gap: 20px;
        }
        h6 {
            color: $orange;
            letter-spacing: 3px;
        }
        .foot-logo {
            scale: .9;
        }
        .socials {
            margin-top: 30px;
            padding-right: 5px;
            color: $silver;
        }
        .menu {
            color: black;
            margin-bottom: 15px;
        }
    }
    margin-bottom: 50px;
}
.last {
    text-align: center;
    background-color: $wood-white;
    a {
        position: absolute;
        left: 20px;
        bottom: calc(50% - 20px);
        text-align: center;
        line-height: 40px;
        width: 40px;
        aspect-ratio: 1 / 1;
        background-color: $text-grey;
        color: white;
        font-size: 1.3rem;
    }
    p {
        font-size: .8rem;
    }
}
</style>