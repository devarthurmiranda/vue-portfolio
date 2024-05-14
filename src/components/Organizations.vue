<template>
    <div class="container-sm container">
        <div class="title">
            <h2>Worked with</h2>
        </div>
        <div class="slides">
            <div class="container-sm container">
                <swiper :slides-per-view="3" :space-between="5">
                    <swiper-slide>
                        <p>Slide</p>
                    </swiper-slide>
                </swiper>
            </div>
        </div>
    </div>

</template>

<script>
import orgs from '../../data/orgs.js';

export default {
    name: 'HomeOrganizations',
    components: {

    },
    data() {
        return {
            orgs: orgs
        };
    }
};
</script>

<style scoped>
.container {
    margin-top: 15%;
    width: 70%;
}

.title {
    margin-bottom: 5%;
}

.slides {
    max-width: 100%;
}

/* Text styles */
h2 {
    text-align: center;
    color: rgb(155, 74, 74);
}
</style>