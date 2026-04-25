<script>
    export default {
        name: "Card",
        props: {
            title: String,
            path: String,
            description: String
        }
    }
</script>

<template>
    <div class="card">
        <img :src="image.path" :alt="image.title">
        <h2>{{ title }}</h2>
        <p>{{ description }}</p>
    </div>
</template>

<style>
    img {
        width: 100%;
        border-radius: 1em;
    }
</style>