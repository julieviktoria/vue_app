<template>

    <header>
        <div>{{ title }}</div>
        <button @click="toggleNavigation">Menu</button>
    </header>

    <nav v-if="isNavigationisible === true">
        <ul>
            <li v-for="page in pages">
                <a href="">{{ page }}</a>
            </li>
        </ul>
    </nav>

</template>

<script>
    export default {
        props: {
            title: {
                type: String,
                default: 'My Website'
            }
        },

        data() {
            return {
                pages: ['Home', 'About', 'Contact'],
                isNavigationVisible: false,
                title
            }
        },

        methods: {
            toggleNavigation() {
                this.isNavigationVisible = !this.isNavigationVisible;
            }
        }
    }
</script>
