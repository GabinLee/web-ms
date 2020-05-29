<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
}
</script>

<style>
*{ margin: 0; padding: 0; box-sizing: border-box; }
html, body{ font-size: 10px; }
a{ display: inline-block; text-decoration: none; color: inherit; }
ul{ list-style: none; }
button{ background-color: transparent; border: none; cursor: pointer; font-size: inherit; }
button:focus{ outline: none; }
img{ display: block; }

.mw1440{ max-width: 1440px; margin: 0 auto; padding: 0 40px; }
.fs12{ font-size: 12px; }
.fs14{ font-size: 14px; }
.fs16{ font-size: 16px; }

.head{ font-size: 46px; }
.title{ font-size: 20px; margin-bottom: 10px; }
.text{ font-size: 14px; margin-bottom: 15px; }

@media (max-width: 1080px) {
  .head{ font-size: 30px; }
}
@media (max-width: 500px) {
  .mw1360{ padding: 0 20px; }
  .text{ margin-bottom: 10px; }
}
</style>