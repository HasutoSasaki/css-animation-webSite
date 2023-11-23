<script setup>
function scrollToTop() {
    alert('トップへ戻る')
}

</script>
<template>
    <div class="arrow-button" @click="scrollToTop"></div>
</template>
<style scoped>
.arrow-button {
    border: 2px solid black;
    border-radius: 50%;
    width: 50px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: fixed;
    right: 20px;
    bottom: 50px;
    z-index: 999;
    box-shadow: 0 3px 10px rgb(0 0 0 / 16%);

}

.arrow-button::before {
    content: "";
    width: 15px;
    height: 15px;
    border: solid;
    border-width: 4px 4px 0 0;
    display: inline-block;
    transform: rotate(-45deg);
    margin-top: 5px;
}

.arrow-button:hover::before {
    border-color: white;
}

.arrow-button::after {
    content: '';
    display: block;
    position: absolute;
    top: 50%;
    left: 50%;
    width: 50px;
    height: 50px;
    background-color: #000;
    border-radius: 50%;
    transform: translate(-50%, -50%) scale(0, 0);
    transition: transform ease 0.4s;
    z-index: -1;
}

.arrow-button:hover::after {
    transform: translate(-50%, -50%) scale(1.1, 1.1);
}
</style>