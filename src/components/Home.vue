
<template>
  <div>
    <h1>Home</h1>
    <nav>
      <router-link to="/" @click="increment">Increment</router-link> |
      <router-link to="/decrement" @click="decrement">Decrement</router-link>
    </nav>
    <router-view/> 
    <p>Current Count: {{ count }}</p>
  </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex';

export default {
  name: 'homeComp',
  computed: {
    ...mapGetters({
      count: 'getCount'
    })
  },
  methods: {
    ...mapActions({
      increment: 'increment',
      decrement: 'decrement'
    })
  }
};
</script>
