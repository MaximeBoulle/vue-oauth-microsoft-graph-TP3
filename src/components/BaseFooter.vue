<template>
    <v-footer class="bg-indigo-lighten-1 text-center d-flex flex-column">
  
      <div class="pt-0">
        This is a footer
      </div>
    
      <div>
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </div>
    </v-footer>
</template>

<style>


</style>

<script>
export default {
    name: 'BaseFooter',
};
</script>
