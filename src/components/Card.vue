<template>
    <div class="card" :key="card.id" v-for="card in cards">
        <IconComponent v-if="type === 'levels'" :colour="'#44bbc4'" :card="card"/>
        <IconComponent v-if=" type==='why'" :colour="'#b64f88'" :card="card"/>
        <div :class="{ 'skillsgrid': type === 'skills' }">
            <div>
                <h3>{{ card.heading }}</h3>
                <h4 v-if="type === 'skills'">Course Description</h4>
                <p>{{ card.body }}</p>
                <h4 v-if="type === 'skills'">Key Learning Objectives</h4>
                <ul v-if="type === 'skills'">
                    <li :key="itemIndex" v-for="(item, itemIndex) in card.objectives">
                        {{ item }}</li>
                </ul>
            </div>
            <img v-if="type === 'skills'" :src="`/public/bgs/${card.img}`">
        </div>
        
    </div>
    
</template>

<script>
import IconComponent from "./Icon.vue"
    export default{
        name:"CardComponent",
        props: {cards: Array , type:String},
        components:{IconComponent}
    }
</script>

