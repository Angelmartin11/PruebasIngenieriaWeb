<template>
  <div id="app">
    <h4 class="bg-primary text-white text-center p-2">
      {{name}}'s Ingredients
    </h4>
    <h3 class="text-black text-center">Storage</h3>
    <div class="container-fluid p-4">
      <div class="row">
        <div class="col font-weight-bold">Ingredient</div>
        <div class="col-2 font-weight-bold">Quantity</div>
      </div>
      <div class="row" v-for="t in ingredients" v-bind:key="t.ingred">
          <div class ="col">{{t.ingred}}</div>
          <div class ="col-2">{{t.quant}}</div>
      </div>
      <br><br>
     <h3 class="text-black text-center">Add Ingredient</h3>
      <div class="row py-2">
        <div class="col">
          <div>
            <label class="text-black text-bold">Name: </label>
            <input v-model="newIngredientText" class="form-control"/>
          </div>
          <div>
            <label class="text-black text-bold">Quantity: </label>
            <input v-model="newIngredientquant" class="form-control"/>
            </div>  
        </div>
      </div>
       <div class="col-2">
          <button class="btn btn-primary" v-on:click="addNewIngredient">Add</button>
        </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      name: "Martin",
      ingredients: [
        {ingred: "Onion",quant: 3},
        {ingred: "Tomato",quant:5}
        ],
      newIngredientText: "",
      newIngredientquant: 0
    }
  },
  methods: {
    addNewIngredient(){
      this.ingredients.push({
        ingred: this.newIngredientText,
        quant: this.newIngredientquant
      });
      this.newIngredientText ="";
      this.newIngredientquant=0;
    }
  }
}
</script>




