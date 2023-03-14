<template>
  <div class="mt-10 text-3xl mx-auto max-w-6xl">
      <Header></Header>
    <div class="mt-10 text-3x1 font-bold">Count: {{count}}</div>
    <div>
      <button v-on:click="addOne" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        Adicionar 1
      </button>
    </div>
    <div className="mt-10">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import Header from "remote/Header";

export default {
  components: {
    Header
  },
  computed: {
    count() {
      return this.$store.state.count;
    }
  },
  methods: {
    addOne(){
      this.$store.commit('addOne')
    }
  }
}
</script>