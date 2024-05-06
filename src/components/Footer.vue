<template>
    <div>
        <footer class="footer">
            <div class="container">
                <div class="row">
                    <div class="col-md-12">
                        <p class="text-center copyright">
                            Arthur Miranda &copy; 2024 All Rights Reserved
                        </p>
                    </div>
                </div>
            </div>
        </footer>
    </div>
</template>

<script>
export default {
    name: 'HomeFooter'
}
</script>

<style>
    .footer{
        position: fixed;
        bottom:0;
        width:100%;
        background-color: #1a1f25;
    }

    .copyright {
        color: white;
    }
</style>