<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12 header-text">
        <h1>Markdown Editor Preview</h1>
        <h4>Zac Baston</h4>
      </div>
    </div>
    <editor></editor>
    <preview></preview>
  </div>
</template>

<script>
import Editor from './components/Editor';
import Preview from './components/Preview';

export default {
  name: 'app',
  components: {
    Editor,
    Preview,
  },
};
</script>

<style>
@import "./assets/style.css";

.markdown-body {
  min-height: 150px;
}
</style>
