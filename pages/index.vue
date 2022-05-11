<template>
  <div>
    <Items></Items>
  </div>
</template>

<script>
import Items from '~/components/Items'
//import Layouts from '~/layouts/default'
//test-rebase-new
//test-rebase-new1

export default {
  components: {
    Items,
   // Layouts,
  },

  async fetch({ store }) {
    await store.dispatch("LOAD_ITEMS", "topstories.json")
  }
}
</script>
