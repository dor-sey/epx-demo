<template>
    <div>
        {{count.a}}
        {{count.b}}
    </div>
</template>

<script>
export default {
  data() {
      return {
      count: {
          a: 1,
        }
      }
  },
  created() {
    setTimeout(() => {
        this.count.a = 2
        setTimeout(() => {
            this.count.b = 2
        }, 1000);
    }, 2000);
  }
}
</script>

<style>

</style>