<template>
  <div class="demo">
    <div class="draggable">
      <draggable v-model="list">
        <transition-group>
          <div v-for="(item, index) in list" :key="index" class="item">{{item}}</div>
        </transition-group>
      </draggable>
    </div>
  </div>
</template>

<script>
import draggable from 'vuedraggable'
export default {
  name: 'Demo',
  components: {
    draggable
  },
  data () {
    return {
      list: ['Leyi', 'so', 'cool']
    }
  }
}
</script>
<style lang="scss" scoped>
.demo {
  background: #e9ecef;
  height: 100vh;
  .draggable {
    margin: 0 auto;
    .item {
      width: 300px;
      background: #fff;
      color: #000;
    }
  }
}
</style>
