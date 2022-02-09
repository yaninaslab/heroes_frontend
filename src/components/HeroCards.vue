<template>
    <div>
<h1>Heroes</h1>
<p>{{ message }}</p>
<section class="hero_container">
    <div v-for="hero in heroes" :key="hero[0]">
        <img :src="hero[5]" :alt="hero[1]">
        <h3>{{ hero[1]}}</h3>
        <p>Secret Identity: {{ hero[2]}}</p>
        <p>Powers: {{ hero[3]}}</p>
        <p>Power Rating: {{ hero[4]}}</p>
    </div>
    
</section>
    </div>
</template>

<script>
import axios from 'axios'

    export default {

        name: "hero-cards",
        data() {
            return {
                heroes: [],
                message: ""
            }
        },
        mounted () {
            axios.request({
                url: "http://127.0.0.1:5000/hero"

            }).then((res) => {
            this.heroes = res.data
            }).catch((err) => {
                console.log(err)
                this.message = "Sorry, something is wrong!"
            })
        },
    }
</script>

<style scoped>
img {
    max-width: 100px;
}
</style>