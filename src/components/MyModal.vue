<template>
    <div>
        <button @click="toggle"> Open Modal </button>
        <teleport to="body">
            <div v-show="show" class = "modal">
                <h1>Title</h1>
                <p>Lorem ipsum dolor</p>
                <button @click="toggle">Close Modal</button>
            </div>
        </teleport>
    </div>
</template>

<script>
export default {
    data() {
        return {
            show: false
        };
    },
    methods: {
        toggle(){
            this.show = !this.show
        }
    }
}
</script>