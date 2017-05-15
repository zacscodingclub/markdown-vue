<template lang="html">
  <div class="col-xs-12 col-md-6 pull-right" id="preview">
    <div class="panel panel-default">
      <div class="panel-body">
        <article class="markdown-body" v-html="renderedMarkdown">
        </article>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  created() {
    Event.$on('convertToMarkdown', (rawText) => {
      /* eslint-disable no-unused-vars */
      /* eslint-disable no-console */
      const data = {
        text: rawText,
        mode: 'gfm',
      };

      this.$http({
        url: 'https://api.github.com/markdown',
        method: 'POST',
        body: data,
      }).then((response) => {
        this.renderedMarkdown = response.data;
      }, (response) => {
        console.log(response.data);
      });
    });
  },
  data() {
    return {
      renderedMarkdown: '',
    };
  },
};
</script>

<style lang="css">
</style>
