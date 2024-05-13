<template>
    <div class="container d-flex justify-content-between">
        <div class="row">
            <div class="col-sm">
                <h2>{{ about.title }}</h2>
                <p>{{ about.content }}</p>
            </div>
            <div class="col-sm ">
                <img class="img-fluid" src="../assets/coding.png" alt="">
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
.container {
    border: 2px solid red;
}

.row {
    margin-top: 200px;
    max-width: 100%;
    text-align: center;
}

/* Image styles */
img {
    width: 300px;
    height: 300px;
}

/* Text styles */
h2 {
    color: #ffffff;
}

p {
    font-size: 18px;
    color: #ffffff;
}
</style>