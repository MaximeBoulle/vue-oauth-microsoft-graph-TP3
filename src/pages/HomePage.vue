<template>
    <div class="home-page">
        <h1>Welcome to the Home Page</h1>
        <p>This is a simple home page for your Vue.js application.</p>
        <BaseButton>Click me!</BaseButton>
    </div>
</template>

<style>

.home-page{
    min-height: 80vh;
}

</style>

<script>

import BaseButton from '@/components/BaseButton.vue';


export default {
    name: 'HomePage',
    components: {
        BaseButton
  }
}
</script>

