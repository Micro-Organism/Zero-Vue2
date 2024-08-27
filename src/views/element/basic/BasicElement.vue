<template>
  <div class="container">
<!--    <layout />-->
    <container />
  </div>
</template>

<script>
import Layout from '@/views/element/components/layout/Layout.vue'
import Container from "@/views/element/components/container/Container.vue";
export default {
  name: 'BasicElement',
  components: { Container, Layout },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
