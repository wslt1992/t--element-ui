<template>
    <button @click="handlerClick"
            class="el-button"
    :class="[
        colorType?'el-button--'+colorType:'',
        size?'el-button--'+size:'',
        {
        'is-round':round
        }
    ]">
        按钮
    </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    colorType: {
      type: String,
      default: 'black'
    },
    round: Boolean,
    size: {
      type: String,
      default: 'normal'
    }
  },
  methods: {
    handlerClick (evt) {
      this.$emit('click', evt)
    }
  }
}
</script>

<style lang="scss" scoped>
    .el-button--red {
        color: black;
    }

    .el-button--red {
        color: red;
    }

    .el-button--blue {
        color: blue;
    }

    .el-button--max {
        width: 100px;
        height: 56px;
    }
    .el-button{
        display: inline-block;
        line-height: 1;
        white-space: nowrap;
        cursor: pointer;
        background: #fff;
        border: 1px solid #dcdfe6;
        color: #606266;
        -webkit-appearance: none;
        text-align: center;
        box-sizing: border-box;
        outline: none;
        margin: 0;
        transition: .1s;
        font-weight: 500;
        -moz-user-select: none;
        -webkit-user-select: none;
        -ms-user-select: none;
        padding: 12px 20px;
        font-size: 14px;
        border-radius: 4px;
    }
    .el-button--normal {
        width: 80px;
        height: 45px;
    }
    .el-button--min {
        width: 60px;
        height: 33px;
    }
    .is-round {
        border-radius: 10px;
    }
</style>
