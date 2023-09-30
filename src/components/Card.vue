<template>
    <div class="card {{group}}" :key="card.id" v-for="card in cards">
        <h3>{{ card.heading }}</h3>
        <p>{{ card.body }}</p>
    </div>
    
</template>

<script>
    export default{
        name:"CardComponent",
        props: {cards: Array, group: String},
    }
</script>

