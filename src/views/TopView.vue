<template>
    <Header />
    <Main />
    <About />
    <AboutSecondary />
    <News />
</template>
<script>

import Header from '../components/Header.vue'
import Main from '../components/main.vue'
import About from '../components/about.vue'
import AboutSecondary from '../components/aboutSecondary.vue'
import News from '../components/news.vue'
export default {
    components: {
        Header,
        Main,
        About,
        AboutSecondary,
        News
    }
}
</script>