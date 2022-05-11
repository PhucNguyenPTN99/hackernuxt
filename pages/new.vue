<template>
  <div>
    <Items></Items>
  </div>
</template>

<script>
import Items from '~/components/Items'
//import Layouts from '~/layouts/default'

export default {
  components: {
    Items,
    //Layouts,
  },

  async fetch({ store }) {
    await store.dispatch("LOAD_ITEMS", "newstories.json")
  }
}
</script>
