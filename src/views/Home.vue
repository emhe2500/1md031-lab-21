<template>
  <div id="backgroundColor">

    <!-- HEADER PART -->
    <div id="upperPart">
      <div id="container">
        <header>
          <img id="headerimg" src="https://bullyssportsbar.com/wp-content/uploads/2014/12/burger-header.jpg">
          <h1 style="color:white" id="headerText">
            ALL SIZE BURGERS</h1>
        </header>
      </div>
    </div>

    <!-- MIDDLE PART -->
    <section>
      <h2 style="color: black" class="Margin"> Select An Amazing Burger</h2>

      <div class="wrapper">
      <div class="wrapper">
        <Burger v-for="burger in burgers"
            v-bind:burger="burger" 
            v-bind:key="burger.name"
                v-on:orderedBurger="addToOrder($event)"/>
  </div>
      </div>
    </section>

    <!-- FORM PART -->

  <main style="clear:left" id="lowerPart" class="Margin" >
    <section id="contact">

      <p>
        <label for="fullname">Full Name</label><br>
        <input type="text" id="firstname" v-model="fn" required="required" placeholder="First -and Last Name">
      </p>
      <p>
        <label for="e-mail">E-Mail</label><br>
        <input type="text" id="lastname" v-model="ln" placeholder="E-mail adress">
      </p>
      <!--
      <p>
        <label for="street">Street</label><br>
        <input type="text" id="streetName" v-model="sn" required="required" placeholder="Street Name">
      </p>
      <p>
        <label for="house">House</label><br>
        <input type="text" id="houseName" v-model="hn" required="required" placeholder="House number">
      </p> */ -->
      <p>
        <label for="payment">Payment Options</label>
        <select id="payment" v-model="rcp">
          <option>Klarna</option>
          <option>Swish</option>
          <option>Credit Card</option>
          <option>AMEX</option>
        </select>
      </p>

      <p>Gender</p>
      <div>
        <input type="radio" id="male" v-model="drone" value="male">
        <label for="male">Male</label>
      </div>

      <div>
        <input type="radio" id="Female" v-model="drone" value="Female">
        <label for="Female">Female</label>
      </div>

      <div>
        <input type="radio" id="Non-binary" v-model="drone" value="Non-binary">
        <label for="Non-binary">Non-binary</label>
      </div>
      <div>
        <input type="radio" id="Undisclosed" v-model="drone" value="Undisclosed">
        <label for="Undisclosed">Non-binary</label>
      </div>
    </section>
  </main>
  </div>

  <!-- MAP -->
  <div class="designMap">
  <div id="map"  v-on:click="setLocation">  <!--setLocation instead of v-on:click="addOrder"-->

    <div v-bind:style="{left: location.x + 'px', top: location.y + 'px'}">
        T
      </div>

  </div>
  </div>

  <!-- BUTTON -->

  <button type="submit" class="MarginButton" v-on:click="order">
    <img src="https://i.pinimg.com/564x/26/39/4f/26394f87c2c357ff58a5e7a547158517.jpg" style="width: 40px">
    Send Info
  </button>

  <!-- FOOTER -->

  <footer style="clear:left">
    <hr/>
    <p>©ALL SIZE BURGERS</p>
  </footer>

<!--

<div id="upperPart">
<div id="container">
<header>
<img id="headerimg" src="https://bullyssportsbar.com/wp-content/uploads/2014/12/burger-header.jpg">
<h1 style="color:white" id="headerText">
  ALL SIZE BURGERS</h1>
</header>
</div>
</div>

<section class="Margin">
<h2 style="color: black" class="Margin"> Select An Amazing Burger</h2>

<div class="wrapper">

<div class="spaceBurgerImg">
  <h2> <big> Big </big> Burger </h2> <a href="https://www.mypokecard.com/my/galery/fBHgK1zJC2s9.jpg" target="_blank">
  <img src="https://scontent.fbma2-1.fna.fbcdn.net/v/t1.18169-9/12715728_1538870369745225_4242224456409900910_n.jpg?_nc_cat=105&ccb=1-5&_nc_sid=9267fe&_nc_ohc=ejMZH5zd-UgAX9noJe8&_nc_ht=scontent.fbma2-1.fna&oh=893fca6b18d0e8566ece9b5e0100673c&oe=61B096B2" alt="Span" title="Another in-line element" width="400" height="300"/>
</a>
  <ul>
    <li> 10000 kCal</li>
    <section class="alergic">
            <span id="idname">
       <li> contains gluten</li>
            </span>
    </section>
  </ul>
</div>

<div  class="spaceBurgerImg">
  <h2> <big>Medium </big>  Burger </h2> <a href="https://www.mypokecard.com/my/galery/fBHgK1zJC2s9.jpg" target="_blank">
  <img src="https://www.chicagotribune.com/resizer/ebv-gQsUlkP06j7qJ4jC9lSUse8=/800x533/top/arc-anglerfish-arc2-prod-tronc.s3.amazonaws.com/public/VINFZCLKLC2VR7KJ3PMEEPVA34.jpg" alt="Span" title="Another in-line element" width="400" height="300"/>
</a>
  <ul>
    <li> 1000 kCal</li>
    <section class="alergic">
            <span id="idname">
            <li> contains lactose</li>
            </span>
    </section>
  </ul>
</div>

<div>
  <h2> <Big> Small </Big> Burger </h2> <a href="https://www.mypokecard.com/my/galery/fBHgK1zJC2s9.jpg" target="_blank">
  <img src="https://www.hyattrestaurants.com/uploaded/recipes/recipe_banner_recipe-1588851476.webp" alt="Span" title="Another in-line element" width="400" height="300"/>
</a>
  <ul>
    <li> 10 kCal </li>
  </ul>
</div>
</div>
</section>

<main style="clear:left" id="lowerPart" class="Margin" >
<section id="contact">

  <p>
    <label for="fullname">Full Name</label><br>
    <input type="text" id="firstname" name="fn" required="required" placeholder="First -and Last Name">
  </p>
  <p>
    <label for="e-mail">E-Mail</label><br>
    <input type="text" id="lastname" name="ln" placeholder="E-mail adress">
  </p>
  <p>
    <label for="street">Street</label><br>
    <input type="text" id="firstname" name="fn" required="required" placeholder="Street Name">
  </p>
  <p>
    <label for="house">House</label><br>
    <input type="text" id="firstname" name="fn" required="required" placeholder="House number">
  </p>
  <p>
    <label for="payment">Payment Options</label>
    <select id="payment" name="rcp">
      <option>Klarna</option>
      <option>Swish</option>
      <option>Credit Card</option>
      <option>AMEX</option>
    </select>
  </p>

  <p>Gender</p>
  <div>
    <input type="radio" id="male" name="drone" value="male"
           checked>
    <label for="male">Male</label>
  </div>

  <div>
    <input type="radio" id="Female" name="drone" value="Female">
    <label for="Female">Female</label>
  </div>

  <div>
    <input type="radio" id="Non-binary" name="drone" value="Non-binary">
    <label for="Non-binary">Non-binary</label>
  </div>
  <div>
    <input type="radio" id="Undisclosed" name="drone" value="Undisclosed">
    <label for="Undisclosed">Non-binary</label>
  </div>
</section>



</main>
<button type="submit" class="MarginButton">
<img src="https://i.pinimg.com/564x/26/39/4f/26394f87c2c357ff58a5e7a547158517.jpg" style="width: 40px">
Send Info
</button>


<footer style="clear:left">
<hr/>
<p>©ALL SIZE BURGERS</p>
</footer>
</div>
-->
</template>

<script>
import Burger from '../components/Burger.vue'
import io from 'socket.io-client'
import menu from '../assets/menu.json'

const socket = io();

/*
function MenuItem (name, imgUrl, kCal, ifLactose,ifGluten) {
this.name = name; // The *this* keyword refers to the object itself
this.img = imgUrl;
this.kCal = kCal;
this.lactose = ifLactose;
this.gluten = ifGluten;
return;
}


const burgerArr = [new MenuItem("smallBurger","https://scontent.fbma2-1.fna.fbcdn.net/v/t1.18169-9/12715728_1538870369745225_4242224456409900910_n.jpg?_nc_cat=105&ccb=1-5&_nc_sid=9267fe&_nc_ohc=ejMZH5zd-UgAX9noJe8&_nc_ht=scontent.fbma2-1.fna&oh=893fca6b18d0e8566ece9b5e0100673c&oe=61B096B2",200,true,false),
new MenuItem("mediumBurger","https://www.chicagotribune.com/resizer/ebv-gQsUlkP06j7qJ4jC9lSUse8=/800x533/top/arc-anglerfish-arc2-prod-tronc.s3.amazonaws.com/public/VINFZCLKLC2VR7KJ3PMEEPVA34.jpg",300,true,false),
new MenuItem("largeBurger","https://www.hyattrestaurants.com/uploaded/recipes/recipe_banner_recipe-1588851476.webp",250,false,false)];
*/

export default {
name: 'Home',
components: {
Burger
},
data: function () {
return {
burgers: menu,
  fn:"",
  ln:"",
  rcp:"Swish",
  drone:"Female",
  orderedBurger:{},
  location: { x: 0,
    y: 0
  }
}
},
  methods: {
  order(){
    console.log(this.fn)
    console.log(this.ln)
    //console.log(this.sn)
    //console.log(this.hn)
    console.log(this.drone)
    console.log(this.rcp)
    console.log(this.orderedBurger);

    socket.emit("addOrder",  { orderId: this.getOrderNumber(),
      details: {
        fn: this.fn,
        ln: this.ln,
        sn: this.sn,
        hn: this.hn,
        rcp: this.drone,
        drone: this.rcp,
        x: this.location.x,
        y: this.location.y
      },
      orderItems: [this.orderedBurger]
        });
  },

    addToOrder: function (event) {
      this.orderedBurger[event.name] = event.amount;
    },

getOrderNumber: function () {
return Math.floor(Math.random()*100000);
},

/*
addOrder: function (event) {
var offset = {x: event.currentTarget.getBoundingClientRect().left,
              y: event.currentTarget.getBoundingClientRect().top};


socket.emit("addOrder", { orderId: this.getOrderNumber(),
                          details: { x: event.clientX - 10 - offset.x,
                                     y: event.clientY - 10 - offset.y },
                          orderItems: ["Beans", "Curry"]
                        }
           );
}, */

    //position of dot on map when ordering
    setLocation: function (event) {
      var offset = {x: event.currentTarget.getBoundingClientRect().left,
        y: event.currentTarget.getBoundingClientRect().top};
      this.location={x: event.clientX - 10 - offset.x,
        y: event.clientY - 10 - offset.y}
    },

}
}
</script>

<style>
#map {
/*width: 1920px;
height: 1078px;
background-image: url("/img/polacks.jpg"); */
  position: relative;
  margin: 0;
  padding: 0;
  background: url(/img/polacks.jpg);
  background-repeat: no-repeat;
  width:1920px;
  height: 1078px;
  cursor: crosshair;
}
#map div {
  position: absolute;
  background: black;
  color: white;
  border-radius: 10px;
  width:20px;
  height:20px;
  text-align: center;
}
/*empty*/
body {
font-family: "Times New Roman";
}

.alergic {
color: #ff5500;
}

.Margin{
margin-left:15px;
}

.MarginButton{
margin-top:20px;
}

.spaceBurgerImg{
padding-right: 60px;
}

.wrapper {
display: grid;
grid-gap: 300px;
grid-template-columns: 33% 33% 33%;
background-color: #eeb482;

}

.designMap{
  overflow: scroll;
  height:500px;
  width:1500px;
  border: 2px dotted #ff9900;
}

#container{
height: 200px;
overflow:hidden;
border: 2px dotted #ff9900;

}

#headerimg{
width: 100%;
height: auto;
opacity: 0.7;
}
#headerText{
position:absolute;
margin-top: -30%;
margin-left:35%;
}

#idname {
text-transform: uppercase;
font-weight: bold;
}

/* gives color to lower and upper part of web site sections*/

#backgroundColor{
  background-color: #FFDEAD;

}

#upperPart {
background-color: #FFDEAD;
color: #8B4513;
}

#lowerPart {
background-color: #ADD8E6;
color: #8B4513;
border: 2px dotted #ff9900;

}

/*button color changes when hover over it accordning to Pseudo-classes*/
button:hover {
background-color: #E9967A;
color: #F0FFF0;
cursor: pointer; /*cursor points when hover over button*/
}
</style>
