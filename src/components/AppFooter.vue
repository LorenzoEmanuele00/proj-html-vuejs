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

</style>