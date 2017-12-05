<template>
    <!-- Editor Textarea -->
    <textarea :value="value" v-focus="focused" id="editor-textarea" class="textarea" placeholder="Let it out here..." @input="$emit('input', $event.target.value)">
    </textarea><!-- End of Editor Textarea -->
</template>

<script>
import autosize from 'autosize'
import { focus } from 'vue-focus'

export default {
  name: 'Editor',
  props: {
    value: {
      default: '',
      type: String
    }
  },
  directives: { focus: focus },
  data () {
    return {
      focused: true
    }
  },
  mounted: function () {
    // Allows textarea to expand indefinitely with text input
    autosize(this.$el)
  }
}
</script>

<style lang="scss" scoped>
    /* Overwrite and to Bulma's textarea class */
    #editor-textarea {
        border: 0;
        box-shadow: none;
        padding: 58px 20%;
        display: inline-block;
        overflow-y: visible;
    }

    /* Remove textarea max-height */
    .textarea:not([rows]) {
        max-height: none;
    }

    /* Media Query for Max-Width 480px */
    @media (max-width: 480px) {
        #editor-textarea {
            padding: 50px 10%;
        }
    }
</style>
