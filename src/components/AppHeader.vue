<script>
export default {
    props: {
        menu: Array,
        social: Array,
    },
    data() {
        return {
        }
    }
}
</script>

<template>
<div class="my_container">
    <section class="social-links d-flex justify-content-between my-3">
        <div>
            <a class="pe-4" href="">Download App <span class="orange px-1">iOS</span></a>
            <a href="">Advertise with us</a>
        </div>
        <div>
            <a v-for="link in social" href="" :class="link" class="px-3"></a>
        </div>
    </section>
    <div class="d-flex justify-content-around"><img src="../assets/img/avada-food-logo-2x.png" alt="avada food logo"></div>
    <nav class="d-flex justify-content-around align-items-center my_container">
        <a v-for="link in menu" href="" class="d-block menu">{{ link }}</a>
        <i class="fa-solid fa-magnifying-glass search-lens mb-3"></i>
    </nav>
</div>
<div class="position-relative text-center">
    <div class="square sq1">
        <i class="fa-brands fa-atlassian"></i>
        <p class="m-0">Demos</p>    
    </div>
    <div class="square sq2">
        <h6 class="price m-0" ><span class="value">$</span>39</h6>
        <p class="m-0">On Sale</p>
    </div>
</div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables.scss" as *; 

.social-links {
    font-size: .8rem;
    a {
        color: $text-grey;
    }
    .orange {
        display: inline-block;
        background-color: $orange;
        border-radius: 2px;
        color: white;
    }
}
img {
    scale: .7;
}
.menu {
    color: black;
    height: 45px;
    &:hover {
        color: $orange;
        border-bottom: 3px solid $orange;
    }
}
.square {
    position: absolute;
    right: 10px;
    width: 70px;
    aspect-ratio: 1 / 1;
    border-radius: 10px;
    padding: 5px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    p {
        font-size: .7rem;
    }
    &.sq1 {
        top: -110px;
        padding-top: 10px;
        i {
            scale: 2;
        }
        p {
            padding-top: 10px;
        }
    }
    &.sq2 {
        top: -30px;
        .price {
            font-size: 2.1rem;
            font-weight: bold;
            color: $ok-green;
            .value {
                font-size: .9rem;
                position: relative;
                top: -15px;
            }
        }
        
    }
}
</style>