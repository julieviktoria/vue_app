<template>
    <div :data-mm="cm">mm: {{ mm }}</div>
    <div>cm: {{ cm }}</div>
    <div>m: {{ m }}</div>
</template>

<script>
    export default {
        props: {
            input: { 
                type: Number, 
                default: 1000 
            }
        },

        data() {
           return {
               mm: 1000
            }
        },

        computed: {
            cm(){
                return this.mm / 10;
            }, 

            m() {
                return this.inCentimeters / 100;
            }
        }
    }
</script>
