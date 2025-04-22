<template>
  <div>{{ passedTestLabel }}</div>
</template>

<script>
import { defineComponent, ref } from "vue"

export default defineComponent({
  name: "JSJamboard",
  data() {
    return {
      ref
    }
  },
  props: {
    passedTestLabel: String
  }
})

</script>
