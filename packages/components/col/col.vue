<script>
export default {
  name: 'Col',
  props: {
    tag: {
      type: String,
      default: 'div'
    },
    col: {
      type: Number,
      default: 24
    },
    offset: {
      type: Number,
      default: null
    }
  },
  render (h) {
    return h(this.tag, {
      class: [
        'imax__col',
        `imax__col--${this.col}`,
        this.offset ? `imax__col--offset-${this.offset}` : ''
      ]
    }, this.$slots.default);
  }
};
</script>
