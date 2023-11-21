<script>
export default {
    data() {
        return {
            animationDelay: 0.1,
            letters: ['L', 'E', 'A', 'R', 'N', 'Y', 'O', 'U', 'R', 'C', 'A', 'R', 'E', 'E', 'R'],
            letters2: ['C', 'A', 'R', 'E', 'E', 'R'],
        }
    },
    methods: {
        incrementDelay() {
            this.animationDelay += 0.1;
        }
    },
    mounted() {
        this.incrementDelay()
    }
}
</script>

<template>
    <div class="main">
        <div class="main__inner">
            <h1>
                <template v-for="(letter, index) in letters" :key="index">
                    <span class="animation" :style="{ animationDelay: index * 0.1 + 's' }">{{
                        letter
                    }}
                        <span v-if="index == 4">&nbsp;</span>
                    </span>
                    <br v-if="index == 8" />
                </template>
                <!-- <span v-for="(letter, index) in letters" :key="index" class="animation"
                    :style="{ animationDelay: index * 0.1 + 's' }">{{ letter }}
                    <span v-if="index == 4">&nbsp;</span>
                </span>
                <br />
                <span v-for="(letter, index) in letters2" :key="index" class="animation"
                    :style="{ animationDelay: index * 0.1 + 's' }">{{ letter }}
                </span> -->
            </h1>
            <div>

            </div>
        </div>
    </div>
</template>

<style scoped>
@keyframes moveUp {

    /* background-color: #5e6060; */
    0% {
        opacity: 0;
        transform: translateY(100px);
    }

    30% {
        opacity: 1;
    }

    100% {
        opacity: 1;
        transform: translateY(0px);
    }
}

.main__inner {
    max-width: 1200px;
    padding: 0 30px;
    margin: 0 auto;
}

.animation {
    opacity: 0;
    animation: moveUp 2.5s ease;
    animation-fill-mode: forwards;
}

span {
    display: inline-block;
}


.main__inner h1 {
    font-size: 64px;
    text-align: right;
    font-family: YuMincho, 游明朝体;

}
</style>