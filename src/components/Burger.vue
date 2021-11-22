<template>
  <div>
    <figure>
    <h2> {{ burger.name }}  </h2>
    <img v-bind:src="burger.img" alt="burgerIMG" style="width:300px; height: 300px">
    <ul>
      <section class="ingredients">
        <li> {{burger.kCal}} kCal</li>
               <span v-if="burger.lactose==true"> <li> <span id="alergies"> contains lactose</span> </li></span>
               <span v-if="burger.gluten==true"> <li> <span id="alergies"> contains gluten</span> </li></span>
      </section>
    </ul>
    <button class="button" v-on:click="decreaseNumb"> - </button>
      {{ amountOrdered }}
      <button class="button" v-on:click="increaseNumb"> + </button>

    </figure>

  </div>
</template>

<script>
export default {
  name: 'Burger',
  props: {
    burger: Object
  },
  data: function () {
    return {
      amountOrdered: 0,
    }
  },methods: {
    increaseNumb(){
      this.amountOrdered = this.amountOrdered +1;
      this.$emit('orderedBurger', { name:   this.burger.name,
        amount: this.amountOrdered
      })
    },
    decreaseNumb(){
      if(this.amountOrdered>0) {
        this.amountOrdered = this.amountOrdered - 1;
        this.$emit('orderedBurger', { name:   this.burger.name,
          amount: this.amountOrdered
        })
      }
    }
  },
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>

.ingredients{
  color: #170b0b;
}
#alergies{
  color: #f64c4c;
  text-transform: uppercase;
}

.button{

}


</style>
