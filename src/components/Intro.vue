<template>
    <div class="container">
        <div class="row align-items-center">
            <div class="col-xl-6 col-bg-6 col-md-6 col-sm-12 text-center">
                <img class="img-me" src="../assets/euu.png"/>
            </div>
            <div class="col-xl-6 col-bg-6 col-md-6 col-sm-12 text-center">
                <h1>Hi, I'm Arthur Miranda!</h1>
                <p>
                    a 4th year computer science student at the Federal Institute Goiano.
                </p>
                <p>
                    I'm currently looking for new opportunities. If you'd like to work together, please don't hesitate to reach out.
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

<style>
    .container {
        padding-top: 100px;
        padding-bottom: 400px;
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