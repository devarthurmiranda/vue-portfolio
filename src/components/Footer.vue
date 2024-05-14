<template>
    <footer class="bg-dark">
        <div class="container-sm container">
            <div class="row">
                <div class="col-sm">
                    <p>
                        Arthur Miranda &copy; 2024 All Rights Reserved
                    </p>
                </div>
                <div class="col-sm">
                    <p>
                        {{ info.email }}
                    </p>
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
</style>