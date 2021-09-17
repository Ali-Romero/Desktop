<template>
  <template v-for="(folder, index) in structure.folders">
    <Item mode="folder" :name="folder.name" @click.prevent="onClick(index)" />
  </template>

  <template v-for="file in structure.files">
    <Item mode="file" :name="file.name"/>
  </template>
</template>

<script>
import Item from "./Item";

export default {
  name: 'FolderView',
  emits: ['open'],
  components: {
    Item,
  },
  data() {
    return {
      timer: null,
      counter: 0
    }
  },
  props: {
    structure: {
      type: Object
    }
  },
  methods: {
    onClick(index) {
      this.counter++;

      if (this.counter == 1) {
         this.timer = setTimeout(() => {
            this.counter = 0;
         }, 300);

         return;
      }

      clearTimeout(this.timer);
      this.counter = 0;

      this.$emit('open', index)
    }
  }
}
</script>
