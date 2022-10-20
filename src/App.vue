<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="stylus">
html,body {
  margin: 0;
  padding: 0;
  color: #333;
  background-color: rgb(241 245 249)
}
button, [type='button'], [type='reset'], [type='submit'] {
  -webkit-appearance: button;
  background-color: transparent;
  background-image: none;
  cursor pointer
}
</style>
