<template>
    <div class="intro container-sm">
        <div class="intro-content">
            <div class="image-me">
                <img class="img-fluid" src="../assets/euu.png" alt="Profile" />
            </div>
            <div class="presentation">
                <h1>{{ intro.title }}</h1>
                <p>{{ intro.description }}</p>
                <div class="socials">
                    <a v-for="social in socials" :href="social.link" :key="social.link">
                        <img class="img-socials" :src="social.img" :alt="social.title || 'social link'">
                    </a>
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
.intro {
    padding-top: 10%;
    width: 70%;
    margin: 0 auto;
}

.presentation {
    padding-top: 50px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;
}

.socials {
    padding-top: 3%;
    display: flex;
    justify-content: center;
    gap: 15px;
}

.intro-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 40px;
}


/** Image styles */
.img-fluid {
    width: 70%;
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
.presentation h1 {
    font-size: 40px;
    color: #ffffff;
    font-weight: 600;

}

.presentation p {
    font-size: 18px;
    color: #ffffff;
}

@media screen and (max-width: 768px) {
    .intro {
        width: 90%;
        text-align: center;
        padding-top: 20%;
    }

    .intro-content {
        flex-direction: column;
        align-items: center;
    }

    .presentation {
        padding-top: 30px;
        align-items: center;
        text-align: center;
    }

    .socials {
        justify-content: center;
    }

    .img-fluid {
        width: 60%;
        max-width: 240px;
    }
}
</style>
