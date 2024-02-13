<template>
    <div class="root">
        <h1 v-if="isVisible">{{ message }}</h1>
        <button v-on:click=" sayHello() ">Toggle Visibility</button>
        <h2 v-bind:class="{highLighted: isHighlighted}">{{ title }}</h2>
        <button @click=" toggleHighlighted() ">Toggle Styles</button>

        <input type="text" v-on:blur="handleBlur" v-model="message">
        <ul>
            <li v-for="(item) in list" :key="item.id" >
                {{ item.text }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'MyComponent',
    data() {
        return {
            message: "Hello World from Vue",
            title: "This is my title",
            isHighlighted: false,
            isVisible: true,
            list: [
                {id:1, text: "First item"},
                {id:2, text: "Second item"},
                {id:3, text: "Third item"}
            ]
        }
    },
    methods: {
        toggleVisibility() {
            this.isVisible = !this.isVisible;
        },
        sayHello() {
            alert("Hello!")
        },
            handleBlur() {
      alert("Continue writing!")
      },
      toggleHighlighted() {
        this.isHighlighted  = !this.isHighlighted;
      } 
    }
}
</script>


<style>
.highLighted {
    color: rgb(255, 215, 0);
    font-weight: 700;
}
</style>

