<template>
  <div id="app">
    <div class="container">
      <div>
        <h2>Basic usage</h2>
        <h-input v-model="valor" />
        <h2>Icon Left</h2>
        <h-input icon="fa fa-search" v-model="valor" />
        <h2>Icon Rigth</h2>
        <h-input icon-rigth="fa fa-search" v-model="valor" />
        <h2>Icon Left Rigth</h2>
        <h-input
          icon-left="fa fa-search"
          icon-rigth="fa fa-search"
          v-model="valor"
        />
        <h2>Border All</h2>
        <h-input v-model="valor2" border="10px" />
        <h2>Border Left</h2>
        <h-input v-model="valor2" border="30px 0 0 30px" />
        <h2>Placeholder</h2>
        <h-input v-model="valor3" placeholder="My placeholder" />
        <h2>Maxlength</h2>
        <h-input v-model="valor2" maxlength="10" />
        <h2>Show word limit</h2>
        <h-input v-model="valor2" maxlength="10" show-word-limit />
        <h2>Disabled</h2>
        <h-input v-model="valor2" disabled />
        <h2>clearable</h2>
        <h-input v-model="valor2" clearable />
        <h2>Password</h2>
        <h-input
          v-model="valor4"
          placeholder="Digite sua senha"
          show-password
        />
      </div>
    </div>
  </div>
</template>

<script>
import HInput from './components/Input'

export default {
  name: 'App',
  components: {
    HInput
  },
  data: () => ({
    valor: '',
    valor2: '',
    valor3: '',
    valor4: ''
  })
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.container {
  width: 900px;
  margin: 10px auto;
}
</style>
