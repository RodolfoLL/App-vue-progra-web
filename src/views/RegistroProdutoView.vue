<script>
export default{
  name:'App',
  data(){
  return {
    Nombre: '',
    Categoria: '',
    Precio:'',
    vencimiento:'',
    Cantidad:'',
    UMedida:'',
  
  }
},
  
  methods: {
    enviarFormulario(evt){
      evt.preventDefault();
      localStorage.setItem('Nombre',this.Nombre);
      localStorage.setItem('Categoria',this.Categoria);
      localStorage.setItem('Precio',this.Precio);
      localStorage.setItem('vencimiento',this.vencimiento);
      localStorage.setItem('Cantidad',this.Cantidad);
      localStorage.setItem('UMedida',this.UMedida);

    this.Nombre = ''
    this.Categoria = ''
    this.Precio = ''
    this.vencimiento = ''
    this.Cantidad = ''
    this.UMedida = ''


  }
}
}

</script>

<template>
  <div class="container">
    <h1>Registrar Producto</h1>
    <form @submit="enviarFormulario">
      <div class="row">
        <div class="col-md-4">
          <label htmlFor="Nombre">Nombre Producto</label>
          <input type="text" v-model="Nombre" id="" class="form-control" />
        </div>
        <div class="col-md-4">
          <label htmlFor="Categoria">Categoria</label>
          <select v-model="Categoria" id="" class="form-select">
            <option disabled value="">Seleccione...</option>
            <option value="lacteo">Lacteos</option>
            <option value="Verduras">Verduras</option>
            <option value="Dulces">Dulces</option>
            <option value="frutas">Frutas</option>

          </select>
        </div>
        <div class="col-md-4">
          <label htmlFor="Precio">Precio</label>
          <input type="text" v-model="Precio" id="" class="form-control" />
        </div>
      </div>
      <div class="row">
        <div class="col-md-4">
          <label htmlFor="vencimiento">Vencimiento</label>
          <input type="date" v-model="vencimiento" id="" class="form-control" />
        </div>
        <div class="col-md-4">
          <label hmlFor="Cantidad">Cantidad</label>
          <input type="text" v-model="Cantidad" id="" class="form-control" />
        </div>
        <div class="col-md-4">
          <label htmlFor="UMedida">U.Medida</label>
          <select v-model="UMedida" id="" class="form-select">
            <option disabled value="">Seleccione...</option>
            <option value="cajas">Cajas</option>
            <option value="botellas">Botellas</option>
          </select>
        </div>
      </div>
      <div class="row align-items-center">
        <div class="button">
          <button type="submit" class="btn btn-primary">Registrar Producto</button>
        </div>
      </div>
    </form>
  </div>
</template>

<style scoped>
.container {
  background-color: white;
  height: 90%;
}
.row {
  margin-top: 20px;
}
.button {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 30%;
}
</style>
