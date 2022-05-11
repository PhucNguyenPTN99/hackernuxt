<template>
  <div class="hello">
    <h1>{{ message }}</h1>
    <h1>{{ value }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    message: {
      type: String,
    },
    value: {
      type: String,
    },
  }
}
</script>