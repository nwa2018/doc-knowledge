# vue的input中，如何限制只能输入number

[vue的input中，如何限制只能输入number](https://segmentfault.com/q/1010000007115009)

``` vue
<template>
  <input :value='code' pattern="\d*" type='number' @input='onInput'>
</template>
<script>
export default {
  data () {
    return {
      code: ''
    }
  },
  methods: {
    onInput (e) {
      this.code = e.target.value.replace(/[^\d]/g,'')
    }
  }
}
</script>
```

或者封装成自定义指令
``` js
//<input v-model="num" v-number-only />
Vue.directive('numberOnly', {
    bind: function () {
        this.handler = function () {
            this.el.value = this.el.value.replace(/\D+/, '')
        }.bind(this)
        this.el.addEventListener('input', this.handler)
    },
    unbind: function () {
        this.el.removeEventListener('input', this.handler)
    }
})
```
