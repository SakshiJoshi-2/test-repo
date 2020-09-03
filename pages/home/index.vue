<template>
  <div>
    <h1>Test Repo</h1>
    <h1>home page</h1>
    <a href="home">Home</a>
    {{counter}} {{counter123}}
    <button class="btn btn-sm btn-info" @click="storetest">store test</button>
  </div>
</template>

<script>
import { mapState, mapActions, mapGetters } from 'vuex'
export default {
  computed: {
    ...mapGetters('modules/crudadmin', ['counter', 'conter123']),
    // ...mapState('modules/crudadmin',['counter','conter123']),
  },
  methods: {
    ...mapActions('modules/crudadmin', ['readData']),
    storetest() {
      this.readData({ test: 'hello' })
    },
  },
}
</script>

<style lang="scss" scoped>
</style>