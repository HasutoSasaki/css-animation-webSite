<template>
    <div class="about">
        <div class="about__inner">
            <div class="about__text">
                <div class="about__text__wrapper">
                    <h2>about menu</h2>
                    <p>【（創業者）】は、【（業界の問題点の説明）】のため、【（会社）】をスタートしました。
                        それが【（解決策にたどりつくまで）】の理由です。
                        その過程で、【（マイルストーンや達成したことの共有）】がありました。
                        わたしたちは、【（今後のミッションの表明）】をしていき</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.about__inner {
    max-width: 1200px;
    padding: 0 30px;
    margin: 0 auto;
    margin-bottom: 50px;
}

.about__inner h2 {
    font-size: 38px;
    margin-bottom: 10px;
}

.about__inner p {
    max-width: 400px;
}

.about__text {
    overflow: hidden;
    transform: translateX(-100%);
    transition: transform cubic-bezier(0.215, 0.61, 0.355, 1) 0.5s;
    font-family: YuMincho, 游明朝体;
    animation: fadeInParent 5s ease;
    animation-fill-mode: forwards;

}

.about__text__wrapper {
    display: block;
    transform: translateX(100%);
    transition: transform cubic-bezier(0.215, 0.61, 0.355, 1) 0.5s;
    animation: fadeInChild 5s ease;
    animation-fill-mode: forwards;
}

@keyframes fadeInParent {
    0% {
        transform: translateX(-100%);
    }

    100% {
        transform: translateX(0);
    }
}

@keyframes fadeInChild {
    0% {
        transform: translateX(100%);
    }

    100% {
        transform: translateX(0);
    }
}
</style>