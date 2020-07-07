<template lang="pug">
.gp-input(
  :style="{borderRadius: border}", 
  :class="{isdisabled : disabled}", 
  @mouseover="hover = true"
  @mouseleave="hover = false",
  )
  i.icon(:class="icon || iconLeft", v-if="icon || iconLeft")
  input(
    :type="!isPassword ? 'text' : 'password'", 
    :placeholder="placeholder", 
    :value="value", 
    :required="required",
    :maxlength="maxlength"
    :disabled="disabled"
    @keyup="hover = true"
    @input="updateValue($event.target.value)")
  i.icon(:class="iconRigth", v-if="iconRigth")
  .limit(v-if="showWordLimit && maxlength") 
    |{{value.length}}/{{maxlength}}
  .clearable(v-if="clearable", @click.prevent="clearValue") 
    i.fa.fa-times-circle-o(v-if="hover")
  .clearable(v-if="showPassword", @click.prevent="isPassword = !isPassword") 
    i.fa.fa-eye(v-if="value.length")
</template>

<script>
export default {
  name: 'HInput',
  props: {
    placeholder: {
      type: String
    },
    value: {
      type: String
    },
    required: {
      type: Boolean,
      default: false
    },
    disabled: {
      type: Boolean,
      default: false
    },
    icon: {
      type: String
    },
    iconLeft: {
      type: String
    },
    iconRigth: {
      type: String
    },
    border: {
      type: String,
      default: '33px'
    },
    maxlength: {
      type: Number
    },
    showWordLimit: {
      type: Boolean,
      default: false
    },
    clearable: {
      type: Boolean,
      default: false
    },
    showPassword: {
      type: Boolean,
      default: false
    }
  },
  data: () => ({
    hover: false,
    isPassword: false
  }),
  computed: {},
  methods: {
    clearValue() {
      this.$emit('input', '')
    },
    updateValue(value) {
      this.$emit('input', value)
    }
  },
  created() {
    this.isPassword = this.showPassword
  }
}
</script>

<style lang="scss" scoped>
.gp-input {
  border: 1px solid #c8d2df;
  height: 50px;
  display: flex;
  justify-content: space-between;
  padding-left: 20px;
  padding-right: 20px;
  .icon {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 40px;
    text-align: center;
    font-size: 24.39px;
    color: #0180ff;
  }
  .clearable {
    color: #909399;
    font-size: 14px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  input {
    border: none;
    font-size: 18px;
    line-height: 40px;
    outline: none;
    width: 100%;
    &::placeholder {
      color: #c8d2df;
    }
    &:disabled {
      background-color: transparent;
    }
  }
  .limit {
    color: #909399;
    font-size: 14px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
.isdisabled {
  background-color: #f6f6f6;
}
</style>
