<template>
    <div class="introduction">
        <div class="introduction__inner">
            <h1 class="introduction-title">Contact introduction</h1>
            <p class="introduction-text">
                cssのoffset-pathプロパティを使ってアニメーションを作りました。
            </p>
            <div class="rollerCoster">
                <div class="rollerCoaster__vehicle">

                    <span class="rollerCoaster__vehicle__item" v-for="index in 5"
                        :style="{ '--index': (index - 1) + ';', 'animation-delay': 'calc(0.5s * var(--index))' }"></span>
                    <span class="rollerCoaster__rail"></span>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
.introduction__inner {
    background-color: black;
}

.introduction-title {
    color: white;
    font-size: 38px;
    margin-left: auto;
    width: fit-content;
    padding-right: 30px;
    padding-top: 20px;
}

.introduction-text {
    color: white;
    width: fit-content;
    margin-left: auto;
    padding-right: 30px;
}

.rollerCoaster {
    pointer-events: none;
    position: relative;
}


.rollerCoaster__vehicle {
    position: relative;
    width: 100%;
    height: 500px;
}

.rollerCoaster__vehicle__item {
    position: absolute;
    display: block;
    width: 20px;
    height: 15px;
    z-index: 10;
    margin-left: 10px;
    background-color: white;
    border-radius: 2px;
    /* offset-path: path("m2.63,209.053C52.632,174.606,73.712,77.114,132.52,52.907c74.773-30.779,12.771,192.822,73.211,202.529,54.714,8.787,52.963-109.401,107.94-109.401,25.342,0,37.3,45.413,41.674,61.454,11.961,43.86,53.559,62.85,70.843,67.476,38.803,10.386,86.598,3.102,110.783-7.36,35.38-15.305,63.534-40.31,79.3-75.913,8.186-18.486,26.224-109.706-43.594-110.659-55.836-.762-59.496,65.968-46.686,99.027,35.952,92.781,261.608,68.707,261.608,68.707V114.533c-96.886-8.899-77.985,90.427-151.986,100.397-33.848,4.56-38.351-89.16-72.384-86.308-32.323,2.709-28.707,116.35-76.631,107.791-18.446-3.294-22.221-82.948-53.338-79.039-46.123,5.794-54.515,96.254-87.623,97.405-99.677,3.467-73.265-152.889-131.541-151.449-41.27,1.02-77.234,61.548-94.523,94.17C78.307,275.366,31.004,272.669,1.6,274.757"); */
    /* offset-path: path("m102,265c0,0 85,70 249,69c164,-1 222,88 222,88c0,0 1,34 1,34c0,0 -173,-40 -220,-1c-47,39 -260,34 -260,34c0,0 8,-224 8,-224z"); */
    offset-path: path("m1,35c120.075,105.71314 339,100 406,98c67,-2 280,135 429,93c-29,65 -333,124 -423,113c-90,-11 -275,78 -410,69c-58.5,-307.5 -41,-387.5 -2,-373z");
    animation: move 14s infinite linear;
    /* animation-delay: calc(0.1s * var(--index)); */
}

@keyframes move {
    to {
        offset-distance: 100%;
    }
}
</style>