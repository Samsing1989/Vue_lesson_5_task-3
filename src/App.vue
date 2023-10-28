<template>
  <notebooks-panel :NotebooksListData="notebooksList" />
</template>

<script>
import NotebooksPanel from "./components/NotebooksPanel.vue"
import { notebooksList } from "./constants/3_data_notebooks"
export default {
  name: "App",
  components: {
    NotebooksPanel,
  },
  data() {
    return {
      notebooksList,
    }
  },
}
</script>

<style></style>
