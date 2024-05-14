<template>
    <div>
        <nav class="navbar navbar-dark bg-dark navbar-expand-lg fixed-top">
            <div class="navbar-brand">
                <a href="/">
                    <Logo />
                </a>
            </div>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation"><span class="navbar-toggler-icon"></span></button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item ms-auto mx-2">
                        <a class="nav-link" href="#about">About</a>
                    </li>
                    <li class="nav-item ms-auto mx-2">
                        <a class="nav-link" href="#organizations">Jobs</a>
                    </li>
                    <li class="nav-item ms-auto mx-2">
                        <a class="nav-link" href="#projects">Projects</a>
                    </li>
                    <li class="nav-item ms-auto mx-2">
                        <a class="nav-link" href="#skills">Skills</a>
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
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    border-bottom: 2px;
}

.navbar-toggler {
    margin-right: 10%;
}

.navbar-brand {
    margin-left: 15%;
}

.navbar-nav {
    margin-right: 10%;
}

/* Text styles */
.navbar a {
    color: white;
    text-decoration: none;
}

.navbar a:hover {
    text-decoration: none;
    color: rgb(155, 74, 74);
}
</style>