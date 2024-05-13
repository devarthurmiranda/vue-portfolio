<template>
    <div class="logo-div">
        <span class="title-span">
            {{ title }}
        </span>
    </div>
</template>

<script>
import logo from '../../../data/logo';

export default {
    name: 'HomeLogo',
    data() {
        return {
            title: logo.title
        }
    }
}


</script>

<style scoped>
.logo-div:hover .title-span {
    letter-spacing: 0px;
    transition: 0.5s all;

}

.title-span {
    font-size: 30px;
    letter-spacing: 2px;
    font-weight: bold;
    transition: 0.5s all;
}
</style>