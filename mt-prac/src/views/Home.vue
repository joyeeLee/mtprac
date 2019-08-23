<template>
  <div class="home">
    <header></header>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
// import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Component({
  components: {
    // HelloWorld
  },
})
export default class Home extends Vue {}
</script>
<style lang="less" scoped>
.home {
  header {
    width: 100%;
    height: 50px;
    padding-left: 10px;
    padding-right: 10px;
  }
}
</style>