<template>
    <Header />
    <Main />
    <About />
    <AboutSecondary />
    <News />
    <PageTopButton />
    <Introduction />
</template>
<script>

import Header from '../components/Header.vue'
import Main from '../components/main.vue'
import About from '../components/about.vue'
import AboutSecondary from '../components/aboutSecondary.vue'
import News from '../components/news.vue'
import PageTopButton from '../components/atoms/PageTopButton.vue'
import Introduction from '../components/Introduction.vue'
export default {
    components: {
        Header,
        Main,
        About,
        AboutSecondary,
        News,
        PageTopButton,
        Introduction
    }
}
</script>
<style scoped></style>