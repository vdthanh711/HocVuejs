<template>
    <div class="TemplateRefs">
        <input ref="input">
    </div>
</template>

<script>


export default {
  name: 'TemplateRefs',
  props: {
    msg: String
  },
  mounted() {
    this.$refs.input.focus()
  }
}
</script>

<style scoped>
  
</style>