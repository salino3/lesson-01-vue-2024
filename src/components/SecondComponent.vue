<template>
    <div id="app">

        <h1>{{ message }}</h1>
        <button @click="changeMessage">Change Message</button>
</div>
</template>


<script>
import {mapState, mapMutations} from 'vuex';

export default {
        name: 'SecondComponent',
    computed: {
        ...mapState(['message'])
    },
    methods: {
        ...mapMutations(['setMessage']),
        changeMessage() {
            this.setMessage("Hello everyone!")
        }
    }
}



</script>