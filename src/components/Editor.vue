<template lang="html">
  <div class="col-xs-12 col-md-6">
    <textarea id="editor" class="form-control" v-model="rawMarkdown"></textarea>
    <button type="button"
            class="btn btn-primary"
            @click="renderPreview">See Preview</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      rawMarkdown: '',
    };
  },
  methods: {
    renderPreview() {
      Event.$emit('process', this.rawMarkdown);
    },
  },
};
</script>

<style lang="css">
</style>
