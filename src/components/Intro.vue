<template>
    <div class="container-sm container d-flex justify-content-between">
        <div class="row">
            <div class="col-sm image-me ">
                <img class="img-fluid" src="../assets/euu.png" />
            </div>
            <div class="col-sm presentation">
                <h1>{{ intro.title }}</h1>
                <p>{{ intro.description }}</p>
                <div class="socials">
                    <a v-for="social in socials" :href="social.link" :key="social"><img class="img-socials" :src="social.img" alt="github"></a>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
import intro from '../../data/intro.js'
import socials from '../../data/socials.js'
export default {
    name: 'HomeIntro',
    data() {
        return {
            intro: intro,
            socials: socials
        };
    }
}
</script>

<style scoped>
.container {
    padding-top: 10%;
    width: 70%;
}

.presentation {
    padding-top: 50px;
}

.row {
    max-width: 100%;
}

.socials {
    padding-top: 3%;
    text-align: center;
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



.img-fluid:hover {
    transition: 400ms;
    border: 5px solid rgb(155, 74, 74);
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