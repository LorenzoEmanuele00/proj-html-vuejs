<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
<div class="hero d-flex justify-content-center align-items-center position-relative">
    <div class="hero-text text-center rounded-3">
        <h2 class="pt-5">Food Corner: Top Japanese Restaurants for sushi</h2>
        <p class="pt-2">March 25, 2019</p>
    </div>
    <div class="orange-top py-2 px-4 rounded-3">TODAY'S PICK</div>
</div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables.scss" as *; 
.hero {
    background-image: url('../assets/img/single-post-img3.jpg');
    background-position: center;
    background-size: 100%;
    min-height: 500px;
    .hero-text {
        background-color: white;
        width: 500px;
        height: 200px;
    }
    .orange-top {
        background-color: $orange;
        color: white;
        font-size: .9rem;
        font-weight: bold;
        position: absolute;
        top: 130px;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    }
}

</style>