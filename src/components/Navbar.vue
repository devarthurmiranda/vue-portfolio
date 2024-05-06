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

<style>
    .navbar {
        background-color: #273848;
        box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }

    .navbar a {
        text-decoration: none;
        color: white;
    }

    .navbar-brand{
        margin-left: 150px;
    }
    
    .navbar-nav{
        margin-right: 150px;
    }
</style>