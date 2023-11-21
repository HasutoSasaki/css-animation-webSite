<template>
    <header class="header">
        <div class="header__inner">
            <h1>HASUTO COMPANY</h1>
            <nav>
                <ul>
                    <li><a href="">ABOUT</a></li>
                    <li><a href="">FOUNDATION</a></li>
                    <li><a href="">STRATEGY and TACIC</a></li>
                    <li><a href="">ACTION</a></li>
                    <li><a href="">MESSAGE</a></li>
                </ul>
                <button>Lean More
                </button>
            </nav>
        </div>
    </header>
</template>
<style scoped>
.header__inner {
    display: flex;
    max-width: 1200px;
    padding: 0 30px;
    margin: 0 auto;
    justify-content: space-between;
    align-items: center;
    height: 100px;
}

.header__inner a {
    position: relative;
    overflow: hidden;
    display: inline-block;
}

.header__inner a::before {
    content: '';
    position: absolute;
    border: solid 1px;
    bottom: 0;
    left: 0;
    width: 0%;
}

.header__inner a:hover {
    width: 100%;
}

.header__inner h1 {
    font-size: 28px;
}

nav {
    display: flex;
    gap: 30px;

}

ul {
    display: flex;
    gap: 20px;
    align-items: center;
}

button {
    background-color: black;
    color: white;
    border-radius: 20px;
    padding: 10px 20px;
    width: fit-content;
    display: flex;
    align-items: center;
}


button::after {
    content: '';
    width: 15px;
    height: 15px;
    display: inline-block;
    box-sizing: border-box;
    border: solid;
    border-width: 3px 3px 0 0;
    transform: rotate(45deg);
    margin-left: 5px;
}
</style>