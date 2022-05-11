<template>
  <div>
    <Items></Items>
  </div>
</template>

<script>
import Items from '~/components/Items'
//import Layouts from '~/layouts/default'
//cmt for test-1
//cmt for test-2

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
