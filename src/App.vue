<template>
  <Layout>
    <template #sidebar>
      <Sidebar />
    </template>

    <template #button>
      <BackButton :disabled="!path" @click="back" />
    </template>

    <template #breadcrumbs>
      <Breadcrumbs>
        {{ computed_path }}
      </Breadcrumbs>
    </template>

    <template #main>
      <FolderView :structure="computed_structure" @open="open" />
    </template>
  </Layout>
</template>

<script>
import Layout from '@/components/Layout.vue'
import FolderView from './components/FolderView.vue'
import Breadcrumbs from './components/Breadcrumbs.vue'
import Sidebar from './components/Sidebar.vue'
import BackButton from './components/BackButton.vue'
import data from './data/list';

export default {
  name: 'App',
  components: {
    Layout,
    FolderView,
    Sidebar,
    Breadcrumbs,
    BackButton,
  },
  data: () => ({
    path: '',
    structure: data
  }),
  computed: {
    computed_structure() {
      if (this.path) {
        return this.path
          .split('.')
          .reduce((acc, current) => acc.folders[current], this.structure)
      }

      return this.structure
    },
    computed_path() {
      if (this.path) {
        let path = ''

        this.path.split('.').reduce((acc, current) => {
          path = `${path} / ${acc.folders[current].name}`

          return acc.folders[current]
        }, this.structure)

        return path
      }

      return '/'
    },
  },
  methods: {
    open(index) {
      this.path = this.path ? `${this.path}.${index}` : `${index}`
    },
    back() {
      const path_arr = this.path.split('.')

      path_arr.pop()

      this.path = path_arr.join('.')
    },
  },
}
</script>
