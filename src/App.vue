<template>
  <div id="app">
    <div id="wrapper">
      <textarea id="source" placeholder="Source" v-model="source"></textarea>
      <div id="output" v-html="format"></div>
    </div>
    
  </div>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    source: '',
  }),
  computed: {
    format() {
      console.log(this.source.replace(/\r/g, '<br />'))
      return this.source.replace(/\r/g, '<br />')
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
#output {
  width: 100%;
  padding: 2px;
  border: 1px solid #000;
  margin-bottom: 10px;
  white-space: pre-wrap;
}
</style>
