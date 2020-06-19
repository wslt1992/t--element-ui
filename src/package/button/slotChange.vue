<template>
    <div>
        <div>头</div>
        <div v-if="$slots.default">
            <slot>这是默认内容</slot>
        </div>
        <div>尾</div>
        <button @click="onClick">修改插槽内的内容为 修改</button>
        <button @click="onClickDestroy">destroy</button>
    </div>
</template>

<script>
export default {
  name: 'slotChange',
  props: {
    text: {
      type: String,
      default: null
    }
  },
  data () {
    return {
      changeSlot: this.text
    }
  },
  beforeDestroy () {
    this.$el.parentElement.removeChild(this.$el)
  },
  methods: {
    onClick () {
      const h = this.$createElement
      const vnode = h('div', '999999999999999')
      this.$slots.default = [vnode]
      this.$forceUpdate()
      // this.changeSlot = 'REPLACED_BY_VNODE'
    },
    onClickDestroy () {
      this.$destroy()
    }
  }
}
</script>

<style scoped>

</style>
