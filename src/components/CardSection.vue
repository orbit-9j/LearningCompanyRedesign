<template>
    <section :id="id">
        <h2>{{ heading }}</h2>
        <div class="grid">
            <CardComponent :cards="cards" :group="sec2"/>
        </div>
    </section>
</template>

<script>
    import CardComponent from '../components/Card.vue';

    export default{
       name: "CardSectionComponent",
       props :{id: String, heading: String, cards:Array, group: String},
       components:{CardComponent},
    }
</script>