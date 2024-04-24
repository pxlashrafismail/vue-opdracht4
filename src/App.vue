<script>
export default{
  data(){
    return{
      title: "Vue fundementals ",
      intro: "lorem ipsum...",
      linkUrl: "http://vuejs.org",
      imageUrl: "../src/assets/images/Vue.js_Logo.png",
      urlUp: "/src/assets/images/up.png",
      fullName: "Ashraf Ismail",
      age: 38,
      visibility: "display: none",
      change: "wijzeggen",
      changed: "gewijzegd",
      testing:"im ganna test now",
      testSucceeded:"good job Ash"
    }
  },
  methods: {
       paragraafAanpassen(){
      let randomNumber  = Math.random();
        if(randomNumber<0.5){
          return "Wij verkopen je de beste producten die je op de markt kan vinden"
      } else{
        return "Wie zoekt die vindt"
      }
    },
    showRandom(){
      return Math.random();
    },
    deleteMe(){
      // let btnDel = document.getElementById('btn-del');
      // btnDel.style.display="none";
      this.visibility="display: none"
    },
    btnShow(){
      // let btnDel = document.getElementById('btn-del');
      // btnDel.style.display="inline-block";
      this.visibility="display: inline-block"

    },
    changeFotoChangeText(){
      let fotoLink = document.getElementById('go-up');
      let btnChange = document.getElementById('btn-change');
      if(fotoLink.src!= this.urlUp && btnChange.innerText===this.change){
        fotoLink.src = this.imageUrl;
        fotoLink.width = "100";
        btnChange.innerText =this.changed;
      } else  {
        fotoLink.src = this.urlUp;
        btnChange.innerText =this.change;
      }
    },
    testingTextChange(){
      let btnTest= document.getElementById('btn-test');
      if(btnTest.innerHTML === this.testing){
        btnTest.innerHTML = this.testSucceeded
      }else{
        btnTest.innerHTML = this.testing

      }
    }
  }
}
</script>

<template>
  <h1>{{ title }}</h1>
  <p>{{ intro.toUpperCase() }}</p>
  <a :href="linkUrl" target="blank">
    <img :src="imageUrl" alt="logo" width="200"/>
  </a>
  <p>{{ paragraafAanpassen() }}</p>
  <hr>
  <h2>Full name: {{ fullName }} </h2>
  <p>age: {{ age }} </p>
  <p>age+5: {{ age +5}} </p>
  <p>random: {{ showRandom()}} </p>
  
  <div>
    <a :href="linkUrl" id="">link naar vue</a>
  </div>
  <div>
    <input type="text" id="name" :value="fullName">
  </div>
  <a href="#" target="blank">
    <img @click="btnShow()" :src="imageUrl" alt="logo" width="200"/>
  </a>
  <button id="btn-del" :style="visibility" @click="deleteMe">Verberg mij</button>
  <hr>
  <hr>
  <a href="#">
    <img id="go-up" :src="urlUp" width="200" alt="">
  </a>
  <button id="btn-change" @click="changeFotoChangeText">{{change}}</button>
  <hr>
  <button id="btn-test" @click="testingTextChange">{{ testing }}</button>
</template>

<style>
</style>