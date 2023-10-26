<script>
export default{
  props:['title'],
  emits:['enlarge-text']
}
</script>
<template>
  <h2>{{ title }}</h2>
  <button @click="$emit('enlarge-text')">텍스트 확대</button>
</template>