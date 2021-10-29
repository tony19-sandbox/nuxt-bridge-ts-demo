<template>
  <button @click="toggle">Toggle {{active}}</button>
</template>

<script lang="ts">
import { defineComponent } from '#app'

export default defineComponent({
  data() {
    const active:boolean = false;
    return {
      active
    }
  },
  methods: {
    toggle(): void {
      this.active = !this.active
    },
  },
})
</script>
