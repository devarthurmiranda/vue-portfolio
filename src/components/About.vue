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

@media screen and (min-width: 768px){
    .container {
        width: 70%;
        padding-top: 4%;
    }
}

.container {
    margin: 0 auto;
}

.row {
    margin-top: 200px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 40px;
}

.description {
    width: 80%;
    display: flex;
    flex-direction: column;
    gap: 15px;
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

@media screen and (max-width: 768px){
    .container {
        width: 90%;
        padding-top: 10%;
        text-align: center;
    }

    .row {
        margin-top: 120px;
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    .description {
        width: 100%;
        align-items: center;
    }

    .description p {
        text-align: center;
    }

    .canva {
        margin-top: 30px;
    }

    .img-fluid {
        width: 80%;
        max-width: 260px;
    }
}
</style>
