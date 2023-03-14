<template>
<div>
  <div class="text=3x1 bg-blue-900 text-white p-5 flex">
    <div class="font-bold flex-grow">
      Header
    </div>
    <div>{{count}}</div>
  </div>
</div>
</template>

<script>
export default {
  name: "Header.vue",

  computed: {
    count() {
      return this.$store?.state?.count ?? 0;
    }
  }
}
</script>

<style scoped>

</style>