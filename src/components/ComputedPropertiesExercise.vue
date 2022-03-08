<template>
  <div class="computed-properties-exercise container">
    <div class="row">
      <div class="col-12">
        <div class="border p-1">
          <div class="reverse-message">
            <p>Original Message: {{ state.message }}</p>
            <p>Computed Reversed Message: {{ state.reversedMessage }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import { computed, reactive } from "vue";
export default {
  name: "computed-properties-exercise",
  setup() {
    const state = reactive({
      message: "RACECAR",
      reversedMessage: computed(() =>
        state.message.split("").reverse().join("")
      ),
    });
    return {
      state,
    };
  },
};
</script>


<style scoped>
</style>
