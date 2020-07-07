# input

> Input Component Based On Vue.js

## Installation

``` bash
npm i @jsheber/input -S
```

``` bash
yarn add @jsheber/input
```

## API

| Param     | Description       | Type     | Default |
| --------- | ----------------- | -------- | ------- |
| v-model | Value input | `String` | - |
| placeholder  | Name input | `String` | - |
| required | Leave the mandatory field | `Boolean` | false |
| disabled | disables the field | `Boolean` | - |
| icon | set icon left | `String`  | - |
| icon-left | set icon left | `String` | - |
| icon-rigth | set icon rigth | `String` | - |
| border | set border radius | `String` | '33px' |
| maxlength | maximum to fill in the field | `Number` | - |
| show-word-limit | count word show limit | `Boolean` | false |
| clearable | clearable field | `Boolean` | false |
| show-password | Show password | `Boolean` | false |

## Usage

### Basic usage
``` bash
# example
<template>
  <div id="app">
    <h2>Basic usage</h2>
    <h-input v-model="valor" />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```

### Icon Left
``` bash
# example
<template>
  <div id="app">
    <h2>Icon Left</h2>
    <h-input icon="el-icon-search" v-model="valor" />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```

### Icon Rigth
``` bash
# example
<template>
  <div id="app">
    <h2>Icon Rigth</h2>
    <h-input icon-rigth="el-icon-search" v-model="valor" />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```

### Icon Left Rigth
``` bash
# example
<template>
  <div id="app">
    <h2>Icon Left Rigth</h2>
    <h-input
      icon-left="el-icon-search"
      icon-rigth="el-icon-search"
      v-model="valor"
    />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```

### Border All
``` bash
# example
<template>
  <div id="app">
    <h2>Border All</h2>
    <h-input
      v-model="valor"
      border="10px"
    />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```

### Border Left
``` bash
# example
<template>
  <div id="app">
    <h2>Border Left</h2>
    <h-input
      icon-left="el-icon-search"
      v-model="valor"
      border="30px 0 0 30px"
    />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```

### Placeholder
``` bash
# example
<template>
  <div id="app">
    <h2>Placeholder</h2>
    <h-input
      v-model="valor"
      placeholder="My placeholder"
    />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```

### Maxlength
``` bash
# example
<template>
  <div id="app">
    <h2>Maxlength</h2>
    <h-input
      v-model="valor"
      maxlength="10"
    />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```

### Show word limit
``` bash
# example
<template>
  <div id="app">
    <h2>Show word limit</h2>
    <h-input
      v-model="valor"
      maxlength="10"
      show-word-limit
    />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```

### Disabled
``` bash
# example
<template>
  <div id="app">
    <h2>Disabled</h2>
    <h-input
      v-model="valor"
      disabled
    />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```

### Clearable
``` bash
# example
<template>
  <div id="app">
    <h2>Clearable</h2>
    <h-input
      v-model="valor"
      clearable
    />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```

### Password
``` bash
# example
<template>
  <div id="app">
    <h2>Password</h2>
    <h-input
      v-model="valor"
      placeholder="Digite sua senha"
      show-password
    />
  </div>
</template>

<script>
import HInput from '@jsheber/input'

export default {
  name: 'app',
  components: {
    HInput
  },
  data: () => ({
    valor: ''
  })
}
</script>
```


## License

MIT