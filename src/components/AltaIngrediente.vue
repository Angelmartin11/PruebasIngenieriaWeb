<template>
    <div class="container">
        <div class="form-group">
            <div class="row">
                <div class="col-6">
                    <label for="">Ingrediente</label>
                    <input type="text" class="form-control">
                </div>
                <div class="col-6">
                    <label for="">Precio Presentacion</label>
                    <input type="text" class="form-control">
                </div>
            </div>
            <div class="row">
                <div class="col-4">
                    <label for="">Presentacion</label>
                    <input type="text" class="form-control">
                </div>
                <div class="col-4">
                    <label for="">Unidad de medida</label>
                    <input type="text" class="form-control">
                </div>
                <div class="col-4">
                    <label for="">Merma %</label>
                    <input type="text" class="form-control">
                </div>
            </div>
            <div class="row mt-3">
                <button class="btn btn-block btn-success">Agregar</button>
            </div>
        </div>
    </div>
</template>


<script>
export default {
  name: 'AltaIngrediente',
}
</script>
