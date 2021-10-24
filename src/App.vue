<template>
  <div id="app">
    <div id="wrapper">
      <textarea id="source" placeholder="Source"></textarea>
      <button id="submit">Submit</button>
      <div id="title" v-html="title"></div>
      <div id="story" v-html="story"></div>
    </div>
    
  </div>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    source: '',
    title: '',
    story: '',
  })
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
  margin-bottom: 10px;
}
#title, #story {
  width: 100%;
  padding: 2px;
  border: 1px solid #000;
  margin-bottom: 10px;
}
</style>
