<template>
  <div>
    <notebooks-item
      v-for="card in NotebooksListData"
      :key="card.id"
      :notebooksCardData="card"
    />
  </div>
</template>

<script>
import NotebooksItem from "./NotebooksItem.vue"
export default {
  components: { NotebooksItem },
  name: "NotebooksPanel",
  props: {
    NotebooksListData: {
      type: Array,
      default: () => [],
    },
  },
}
</script>

<style scoped></style>
