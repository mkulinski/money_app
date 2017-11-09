<template>
  <header>
    <v-card-title class="blue white--text">
      <span class="headline">Menu</span>
      <v-spacer></v-spacer>
      <v-menu bottum left>
        <v-btn icon slot="activator" dark>
          <v-icon>more_vert</v-icon>
        </v-btn>
        <v-list>
          <v-list-tile v-for="item in items" :key="item.title">
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile>
        </v-list>
      </v-menu>
    </v-card-title>
  </header>
</template>

<script>
export default {
  name: 'Navigation',
  data() {
    return {
      msg: 'navvv',
      items: [
        { title: 'Link 1' },
        { title: 'Link 2' },
        { title: 'Link 3' },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  header {
    position: fixed;
    width: 100%;
    top: 0;
  }
</style>
