<template lang="">
  <header-item></header-item>
  <content-item></content-item>
</template>


<script>
import HeaderItem from './components/HeaderItem.vue';
import ContentItem from './components/ContentItem.vue';





export default {
  components: {HeaderItem, ContentItem},
}
</script>



<style scoped>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    display: flex;
    flex-direction: column;
  }
</style>