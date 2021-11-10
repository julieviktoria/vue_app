<template> 
    <Navigation :title="`My title from prop`"/>
    <!-- <Converter :input="1000" /> -->
    <!-- <Counter /> -->
</template>

<script>
    import Navigation from '../components/Navigation.vue';
    import Converter from '../components/Converter.vue';
    import Counter from '../components/Counter.vue';

    export default {
        components: {
            Converter,
            Counter,
            Navigation
        },
    };
  
</script>

<style>
    @import '../style/reset.css';
    @import '../style/style.css';
    @import '../style/variables.css';
</style>