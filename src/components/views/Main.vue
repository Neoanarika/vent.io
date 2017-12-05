<template>
    <div id="main-container" class="container-fluid">
      <editor v-model="rant"></editor>
      <delete-button v-if="show" class="trash is-pulled-right" @click.native="clearRant"></delete-button>
    </div>
</template>

<script>
import Editor from '../common/Editor'
import DeleteButton from '../common/DeleteButton'

export default {
  name: 'Main',
  components: {
    Editor,
    DeleteButton
  },
  data () {
    return {
      rant: '',
      show: false
    }
  },
  methods: {
    clearRant: function () {
      console.log(`Rant trashed!`)
      this.rant = ''
    }
  },
  watch: {
    rant: function () {
      this.rant.length > 0 ? this.show = true : this.show = false
    }
  }
}
</script>

<style scoped>
  .trash {
    position: fixed;
    right: 5%;
    bottom: 7%;
  }
</style>
