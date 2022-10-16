<template>
  <div class="modal" style="text-align: center">
    <h2>{{ uiState === 'won' ? 'You Won!' : 'You Lost!' }}</h2>
    <h3>{{ uiState === 'won' ? '🏆' : '😞' }}</h3>
    <button @click="reset()">Let's play again!</button>
  </div>
</template>

<script>
import { mapState } from 'vuex';

export default {
  methods: {
    reset() {
      this.$store.commit('reset');
    },
  },
  computed: {
    ...mapState(['uiState']),
  },
};
</script>

<style></style>
