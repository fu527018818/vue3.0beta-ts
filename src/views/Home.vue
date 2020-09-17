<template>
  <div class="home">
    <div>{{ state.double }}</div>
    <div>{{ refCeshi }}</div>
    <div @click="indete">点击我</div>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, computed } from "vue";

export default defineComponent({
  name: "Home",
  components: {},
  setup() {
    const state: Counter = reactive({
      count: 0,
      double: computed(() => state.count * 2)
    });
    function indete() {
      state.count += 2;
    }
    const refCeshi = ref("小花猫");
    return {
      state,
      indete,
      refCeshi
    };
  }
});
</script>
