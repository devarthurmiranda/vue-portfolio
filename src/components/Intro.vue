<template>
    <div class="container">
        <div class="row">
            <div class="col-sm">
                <img class="img-fluid" src="../assets/euu.png" />
            </div>
            <div class="col-sm presentation">
                <h1>{{ intro.title }}</h1>
                <p>{{ intro.description }}</p>
                <div class="socials">
                    <a href=""><img class="img-socials" src="../assets/socials/github.png" alt="github"></a>
                    <a href=""><img class="img-socials" src="../assets/socials/linkedin.png" alt="linkedin"></a>
                    <a href=""><img class="img-socials" src="../assets/socials/youtube.png" alt="youtube"></a>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
import intro from '../../data/intro.js'
export default {
    name: 'HomeIntro',
    data() {
        return {
            intro: intro
        };
    }
}
</script>

<style scoped>
.container {
    padding-top: 100px;
}

.presentation {
    padding-top: 50px;
}

.row {
    text-align: center;
    width: 100%;
}

/** Image styles */
.img-fluid {
    width: 300px;
    height: 300px;
    border-radius: 50%;
    border: 5px solid #ffffff;
}

.img-socials {
    width: 50px;
    margin: 10px;
}


/** Text styles */
.row h1 {
    font-size: 50px;
    color: #ffffff;

}

.row p {
    font-size: 18px;
    color: #ffffff;
}
</style>