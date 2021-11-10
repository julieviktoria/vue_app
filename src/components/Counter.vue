<template>
    <div class="Counter">
        <div class="counter_count">My count: {{ count }}</div>
        
        <div v-if="count > 10">More than 10</div>
        <div v-else-if="count > 5">More than 5</div>
        <div v-else>Neither more than 5 or 10</div>

        <div>{{ timesHundred }}</div>

        <ol :class="isMoreThanTen">
            <li v-for="(fruit, index) in fruits" :key="`f-${index}`">{{ fruit }} {{ index }}</li>
        </ol>

        <div>
            <button class="counter_button" v-on:click="increase">Increase</button>
            <button class="counter-button" v-on:click="decrease">Decrease</button>
        </div>

    </div>
</template>

<script>
    export default {
        
        data() {
           return {
                fruits: ['banana', 'apple', 'melon'],
                count: 0
            }
        },

        computed: {
            isMoreThanTen() {
            },

            timesHundred() {
            }
        },

        methods: {
            increase() {
                this.count += 1;
            },

            decrease() {
                this.count -= 1;
            }
        }
    }
</script>

<style> 
</style>