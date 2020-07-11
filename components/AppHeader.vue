<template>
    <header class="header">
        <h1 class="title">
            Dad Jokes
        </h1>
        <ul>
            <li><nuxt-link to="/">Home</nuxt-link></li>
            <li><nuxt-link to="/jokes">Jokes</nuxt-link></li>
            <li><nuxt-link to="/about">About</nuxt-link></li>
        </ul>
    </header>
</template>

<script>
export default {
    name: "AppHeader"
}
</script>

<style>
    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-bottom: 1px solid #000;
        padding: 1rem;
    }

    .title {
        font-size: 1.5rem;
        color: #000;
    }

    .header ul {
        display: flex;
    }

    .header a {
        display: inline-block;
        margin-right: .5rem;
        padding: .5rem;
    }
</style>