<template>
    <div id="about" class="container-sm container d-flex justify-content-between">
        <div  class="row">
            <div class="col-sm description">
                <h2>{{ about.title }}</h2>
                <p>{{ about.content }}</p>
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
}

.row {
    margin-top: 200px;
    
}

.canva {
    text-align: center;
}


/* Image styles */
.img-fluid {
    width: 100%;
    height: 100%;
}

/* Text styles */
h2 {
    color: rgb(155, 74, 74);
}

p {
    font-size: 18px;
    color: #ffffff;
}
</style>