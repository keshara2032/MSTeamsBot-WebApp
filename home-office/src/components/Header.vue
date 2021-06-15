<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @btn-click="$emit('toggle-status')"
      :text="setStatus ? 'Busy' : 'Available'"
      :color="setStatus ? '#b94242' : '#42b983'"
    />
  </header>
</template>

<script>
import Button from './Button'

export default {
  name: 'Header',
  props: {
    title: String,
    setStatus: Boolean,
  },
  components: {
    Button,
  },

}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
