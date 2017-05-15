<template lang="html">
  <div class="row">
    <div class="col-xs-12 col-md-6">
      <textarea id="editor" class="form-control" v-model="rawMarkdown"></textarea>
    </div>
    <div class="col-xs-12 col-md-6" id="preview">
      <div class="panel panel-default">
        <div class="panel-body">
          <article class="markdown-body">

          </article>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: {
    rawMarkdown: '',
  },
};
</script>

<style lang="css">
</style>
