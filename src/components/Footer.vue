<template>
    <footer class="bg-dark">
        <div class="container-sm container">
            <div class="row">
                <div class="col-sm">
                    <a href="">
                        <p>
                            Arthur Miranda &copy; 2024 All Rights Reserved
                        </p>
                    </a>

                </div>
                <div class="col-sm">
                    <a href="">
                        <p>
                            {{ info.email }}
                        </p>
                    </a>
                </div>
            </div>
        </div>
    </footer>

</template>

<script>
import info from '../../data/footer.js';
export default {
    name: 'HomeFooter',
    data() {
        return {
            info: info
        };
    }
}

</script>

<style scoped>
footer {
    padding-top: 20px;
    bottom: 0;
    left: 0;
    max-width: 100%;
    margin-top: 10%;
}

.row {
    color: white;
    text-align: center;
}

.col-sm a {
    color: white;
    text-decoration: none;
}

.col-sm a:hover {
    text-decoration: none;
    color: rgb(155, 74, 74);
    transition: 400ms;
}
</style>