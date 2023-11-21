<template>
    <div class="aboutSecondary">
        <div class="aboutSecondary__inner">
            <div class="aboutSecondary__bg">
                <div class="aboutSecondary__text">
                    <h2>secondary</h2>
                    <p>このサイトは、<span>一人でも稼げる</span>スキルを身につけるためのリソースです。プログラミングスクールの提供を通じて、未経験者でも挫折しない環境を提供しています。</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.aboutSecondary__inner {
    max-width: 1200px;
    margin: 0 auto;
    color: #fff;
}

.aboutSecondary__bg {
    height: 100%;
    width: 100%;
    padding: 50px 30px;
    position: relative;
}

.aboutSecondary__bg::before {
    content: '';
    background-color: #000;
    position: absolute;
    display: block;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    transform: translate(100%, 0);
    transition: transform cubic-bezier(0.215, 0.61, 0.355, 1) .6s;
    animation: fadeIn 2s ease-in-out;
    animation-fill-mode: forwards;
}

@keyframes fadeIn {
    0% {
        transform: translate(100%, 0);
    }

    100% {
        transform: translate(0, 0);
    }
}

.aboutSecondary__inner h2 {
    position: relative;
    font-size: 38px;
    margin-left: auto;
    padding-bottom: 10px;
    width: fit-content;
    line-height: .9em;

    margin-bottom: 25px;
}

.aboutSecondary__inner h2::before {
    opacity: 0;
    content: '';
    position: absolute;
    width: 190px;
    border: #fff solid 1px;
    bottom: 0;
    right: 0;
    animation-delay: 2s;
    animation-duration: 2s;
    animation-name: borderFadeIn;
    animation-fill-mode: forwards;
}

@keyframes borderFadeIn {
    0% {
        width: 0px;
        opacity: 1;
    }

    100% {
        width: 190px;
        opacity: 1;
    }
}

.aboutSecondary__text {
    margin-left: auto;
    width: 400px;
}

.aboutSecondary__text span {
    background: linear-gradient(transparent 60%, rgba(255, 255, 255, 0.4) 90%);
}
</style>