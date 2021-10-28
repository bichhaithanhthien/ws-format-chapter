<template>
  <div id="app">
    <div id="wrapper">
      <textarea id="source" placeholder="Source" v-model="source"></textarea>
      <p id="output" v-html="format(source)"></p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    source: '',
    output: '',
  }),
  methods: {
    format(source) {
      let output = source.replace(/\\n/g, '<br />')
      output = output.replace(/\\r/g, '')
      output = output.replace(/\\/g, '')
      return output
    }
  },
}
</script>

<style>
#app {
  width: 100%;
  display: flex;
  justify-items: center;
  align-items: flex-start;
}
#wrapper {
  width: 75%;
  max-width: 768px;
}
#source {
  min-width: 100%;
  width: 100%;
  max-width: 768px;
  min-height: 300px;
  height: 300px;
  max-height: 300px;
  outline: none;
  margin-bottom: 5px;
}
#submit {
  margin: 5px 0;
}
#output {
  width: 100%;
  padding: 2px;
  border: 1px solid #000;
  margin-bottom: 10px;
  white-space: pre-wrap;
}
</style>
