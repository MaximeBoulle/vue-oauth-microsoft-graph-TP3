<template>
    <v-btn :disabled="isDisabled" @click="click">
        <slot></slot>
    </v-btn>
</template>

<script>
export default {
    name: 'BaseButton',

    data() {
        return {
            isDisabled: false
        }
    },

    methods: {
        click() {
            this.isDisabled = true;        }
    }
};
</script>

<style scoped>

    .v-btn:hover {
        transform: scale(1.2);
        animation-duration:2s
    }

    .v-btn:focus {
        background: gray;
    }


</style>