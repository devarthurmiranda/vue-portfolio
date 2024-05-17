<template>
    <div id="about" class="container-sm container d-flex justify-content-between">
        <div class="row">
            <div class="col-sm description">
                <h2>{{ about.title }}</h2>
                <p>{{ about.first_paragraph }}</p>
                <p>{{ about.second_paragraph }}</p>
                <p>{{ about.third_paragraph }}</p>
            </div>
            <div class="col-sm canva">
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
    width: 70%;
    padding-top: 4%;
}

.row {
    margin-top: 200px;
    
}

.description {
    width: 80%;
}

.canva {
    text-align: center;
}


/* Image styles */
.img-fluid {
    width: 90%;
    height: 90%;
}

/* Text styles */
h2 {
    color: rgb(155, 74, 74);
    font-weight:600;
}

p {
    font-size: 18px;
    color: #ffffff;
}
</style>