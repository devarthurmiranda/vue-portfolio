<template>
    <div>
        <nav class="navbar navbar-expand-lg fixed-top">
            <div class="navbar-brand">
                <a href="/">
                    <Logo />
                </a>
            </div>
            <div class="collapse navbar-collapse">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item mx-2">
                        <a href="#projects">Projects</a>
                    </li>
                    <li class="nav-item mx-2">
                        <a href="#about">About</a>
                    </li>
                </ul>
            </div>
        </nav>
    </div>
</template>

<script>
import Logo from './helpers/Logo.vue'

export default {
    name: 'NavBar',
    components: {
        Logo
    }
}
</script>

<style scoped>
    .navbar {
        background-color: #17181a;
        box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        border-bottom: 2px;
    }

    .navbar a {
        color: white;
        text-decoration: none;
    }

    .navbar a:hover {
        text-decoration: none;
        color: rgb(155, 74, 74);
    }

    .navbar-brand{
        margin-left: 15%;
    }
    
    .navbar-nav{
        margin-right: 15%;
    }
</style>