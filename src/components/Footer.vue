<template>
    <footer>
        <div class="container">
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
    footer{
        background-color: rgb(73, 69, 69);
        padding-top: 20px;
        bottom: 0;
        left: 0;
        max-width: 100%;
    }

    .container{
        background-color: rgb(73, 69, 69);
    }

    .row{
        color: white;
        text-align: center;
    }
</style>