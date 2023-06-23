<script>
export default {
  created() {
    this.dataLocalSotorage()
  },
  methods: {
    dataLocalSotorage() {
      this.Nombre = localStorage.getItem('Nombre')
      this.Categoria = localStorage.getItem('Categoria')
      this.Precio = localStorage.getItem('Precio')
      this.vencimiento = localStorage.getItem('vencimiento')
      this.Cantidad = localStorage.getItem('Cantidad')
      this.UMedida = localStorage.getItem('UMedida')
    }
  },
  data() {
    return {
      Nombre: '',
      Categoria: '',
      Precio: '',
      vencimiento: '',
      Cantidad: '',
      UMedida: ''
    }
  }
}
</script>

<template>
  <main class="container">
    <h1>Productos</h1>
    <div class="card" style="width:10rem">
      <div class="card-body">
        <h5 class="card-title">{{ Nombre }}</h5>
        <h6 class="card-subtitle mb-2 text-body-secondary">{{ Categoria }}</h6>
        <h6 class="card-subtitle mb-2 text-body-secondary">{{ Precio }}</h6>
        <h6 class="card-subtitle mb-2 text-body-secondary">{{ vencimiento }}</h6>
        <h6 class="card-subtitle mb-2 text-body-secondary">{{ Cantidad }}</h6>
        <h6 class="card-subtitle mb-2 text-body-secondary">{{ UMedida }}</h6>

        
      </div>
    </div>
  </main>
</template>
<style scoped>
.container {
  background-color: white;
  height: 90%;
}
</style>
