<template>
<div class="container">
    <div class="row">
        <div class="col-sm">
            <h2>{{ about.title }}</h2>
            <p>Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum </p>
        </div>
        <div class="col-sm">
            <img src="../assets/coding.png" alt="">
        </div>
    </div>
</div>
</template>

<script>
import about from '../../data/about.js';

export default {
    name: 'HomeAbout',
    data() {
        return {
            about: about
        };
    }
}
</script>

<style scoped>
    img {
        width: 300px;
        height: 300px;
    }

    .container {
        border: 2px solid red;
        text-align: center;
    }

    .row {
        margin-top: 100px;
        text-align: center;
        max-width: 100%;
    }

    h2 {
        color: #ffffff;
    }

    p {
        font-size: 18px;
        color: #ffffff;
    }
</style>