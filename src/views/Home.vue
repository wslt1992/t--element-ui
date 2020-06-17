<template>
  <div class="home">
    <Button color-type="primary" size="mini">按钮</Button>
    <Button color-type="danger" size="mini" round>按钮</Button>
    <Button color-type="blue" size="mini" circle>圆</Button>
    <Button color-type="blue" size="mini" circle></Button>
  </div>
</template>

<script>
// @ is an alias to /src
import Button from '@/package/button/Button'

export default {
  name: 'Home',
  components: { Button }
}
</script>
