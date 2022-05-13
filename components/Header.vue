<template>
    <header>
        <nav>
            <ul>
                <li><nuxt-link to="/">Starting page</nuxt-link></li>
                <li><nuxt-link to="/recipes">Recipes</nuxt-link></li>
                <li><nuxt-link to="/about">About</nuxt-link></li>
            </ul>
        </nav>
    </header>
</template>

<style scoped>
header {
    width: 100%;
    height: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
   
}
ul {
    list-style: none;
    padding: none;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
}
li {
    margin: 0 10px;
    font-family: Arial, Helvetica, sans-serif;
}
a {
    text-decoration: none;
    color: black;
}
</style>