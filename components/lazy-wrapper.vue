
<script>
import Spinner from "~/components/spinner"

export default {
  functional: true,
  props: {
    loading: {
      type: Boolean,
      default: false
    }
  },
  render(h, { props, children }) {
    return props.loading
      ? h("div", { style: { "text-align": "center" } }, [
          h(Spinner, { props: { show: true } })
        ])
      : children
  }
}
</script>
