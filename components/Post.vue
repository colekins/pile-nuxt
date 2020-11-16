<template>
  <div>
    <h1>{{ post.date }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    // eslint-disable-next-line vue/require-default-prop
    post: Object,
  },
}
</script>

<style></style>
