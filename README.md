# vue-bulma-slider

Slider component for Vue Bulma.

Fork of [vue-bulma/slider](https://github.com/vue-bulma/slider)

## Installation

```
$ yarn add https://github.com/Andersbiha/vue-bulma-slider
```


## Examples

```vue
<template>
  <div>
    <slider type="success" size="large" :value="value" :max="100" :step="1" is-fullwidth @change="update"></slider>
    <input class="input" type="number" v-model="value" min="0" max="100" number>
  </div>
</template>

<script>
import Slider from 'vue-bulma-slider'

export default {
  components: {
    Slider
  },

  data () {
    return {
      value: 23
    }
  },

  computed: {
    per () {
      return this.value + '%'
    }
  },

  methods: {
    update (val) {
      this.value = Number(val)
    }
  }

 }
</script>
```
