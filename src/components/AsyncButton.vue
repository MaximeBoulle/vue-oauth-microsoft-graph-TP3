<template>
    <BaseButton :disabled="isDisabled" @click="click">
        <slot></slot>
    </BaseButton>
</template>

<script>

import BaseButton from '@/components/BaseButton.vue';

export default {
    name: 'AsyncButton',
    props: {
        disabled: {
            type: Boolean,
            default: false
        },
        color: {
            type: String,
            default: 'primary',
        },
    },
    data() {
        return {
            isDisabled: this.disabled 
        };
    },
    methods: {
        async click() {
            this.isDisabled = true;
            await this.wait(2000);            
            this.isDisabled = false;
        },

        async wait(time) {
            await new Promise(resolve => setTimeout(resolve, time));
        }
    },
    components: {
        BaseButton
    }
};
</script>

<style scoped>
    .v-btn:hover {
        transform: scale(1.2);
        animation-duration: 2s;
    }
    .v-btn:focus {
        background: gray;
    }
</style>
