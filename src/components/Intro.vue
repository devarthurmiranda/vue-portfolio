<template>
    <div class="container">
        <div class="row align-items-center">
            <div class="col-xl-6 col-bg-6 col-md-6 col-sm-12 text-center">
                <img class="img-me" src="../assets/euu.png"/>
            </div>
            <div class="col-xl-6 col-bg-6 col-md-6 col-sm-12 text-center">
                <h1>Hi, I'm Arthur Miranda!</h1>
                <p>
                    a Software Developer and 4th year Computer Science student at the Federal Institute Goiano.
                </p>
                <div class="socials">
                    <a href=""><img class="img-socials" src="../assets/github.png" alt="github"></a>
                    <a href=""><img class="img-socials" src="../assets/linkedin.png" alt="linkedin"></a>
                    <a href=""><img class="img-socials" src="../assets/youtube.png" alt="youtube"></a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HomeIntro'
}
</script>

<style scoped>
    .container {
        padding-top: 100px;
        padding-bottom: 200px;
    }

    .row h1 {
        font-size: 50px;
        color: #ffffff;
        
    }

    .img-me {
        width: 300px;
        border-radius: 50%;
        border: 5px solid #ffffff;
    }

    .img-socials {
        width: 50px;
        margin: 10px;
    }

    .row p {
        font-size: 18px;
        color: #ffffff;
    }


</style>