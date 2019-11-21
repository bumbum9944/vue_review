<template>
  <div>
      <h5>{{propsLuck.lucky_msg}}</h5>
      <button @click="clickLuck(propsLuck.star)">{{propsLuck.star}}</button>
  </div>
</template>

<script>
export default {
  props: {
    propsLuck: Object
  },
  methods: {
    clickLuck: function(luck){
      const targetURL = `https://search.naver.com/search.naver?where=nexearch&sm=tab_etc&query=${luck}운세`
      console.log(targetURL)
      window.location.href = targetURL
    }
  }
}
</script>

<style>

</style>