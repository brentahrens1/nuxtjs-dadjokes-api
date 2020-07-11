<template>
    <div>
        <nuxt-link to="/jokes" class="back-link">Back to jokes</nuxt-link>
        <h2>{{ joke }}</h2>
        <small>Joke ID: {{ $route.params.id }}</small>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    data() {
        return {
            joke: {}
        }
    },
    async created() {
        const config = {
            headers: {
                'Accept': 'application/json'
            }
        }

        try {
            const res = await axios.get(`https://icanhazdadjoke.com/j/${this.$route.params.id}`, config)
            this.joke = res.data.joke
        } catch (error) {
            console.log(error)
        }
    },
    head() {
        return {
            title: this.joke,
            meta: [
                {
                    hid: "description",
                    name: "description",
                    content: "Best place for corny dad jokes"
                }
            ]
        }
    }
}
</script>

<style>
    .back-link {
        border: 2px solid #000;
        display: inline-block;
        padding: .3rem;
        margin-top: .4rem;
    }

    .back-link:hover {
        background: #000;
        color: #fff;
    }
</style>