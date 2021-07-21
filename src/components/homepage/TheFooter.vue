<template>
  <div class="footer" id="footer">
    BakerihelmOne &copy; {{year}}
  </div>
</template>

<script>
export default {
  name: 'TheFooter',
  data () {
    return {
      year: new Date().getFullYear()
    }
  }
}
</script>
