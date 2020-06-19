<template>
  <div class="home">
    <Button color-type="primary" size="mini">按钮</Button>
    <Button color-type="danger" size="mini" round>按钮</Button>
    <Button color-type="blue" size="mini" circle>圆</Button>
    <Button color-type="blue" size="mini" circle></Button>
    <slot-change></slot-change>
    <slot-change text="插入内容">插入内容</slot-change>
  </div>
</template>

<script>
// @ is an alias to /src
import Button from '@/package/button/Button'
import SlotChange from '@/package/button/slotChange'

export default {
  name: 'Home',
  components: { SlotChange, Button }
}
</script>
