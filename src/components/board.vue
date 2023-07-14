<script>
    export default {
        'name': "Board",
        data() {
            return {
                hello: "Привет",
                wallpaper: [
                "https://klevtsovaelena.github.io/wallpaper/img/Fire6.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Fire7.jpeg",
                "https://klevtsovaelena.github.io/wallpaper/img/Fire8.png",
                "https://klevtsovaelena.github.io/wallpaper/img/Fire9.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Fire10.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Fire11.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Fire12.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower1.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower2.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower3.jpeg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower4.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower5.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower6.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower7.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower8.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower9.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower10.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower11.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Flower12.jpg",
                ],
                currentWallpaper: 0,
                activeMenu: false,
            };
        
    } ,
    props: ['test'],
    methods: {
      changeBackground(number){
        this.currentWallpaper=number;
        //Принудительно закрыть Меню
        this.activeMenu = false;
      },
      openCloseMenu(){
        //alert('Сработала функция openCloseMenu')
        //this.activeMenu = true;
        //Проверить открыто или закрыто сейчас Меню
        if  (this.activeMenu){
        //Если переменная в значении true
        this.activeMenu = false;
        } else {
          this.activeMenu = true;
        }
      }
    }

    }
    
</script>

<template>
<div>
    
    <div class='board' :style="{ 'background-image': `url(${wallpaper[currentWallpaper]})`}" >
      <button class='board__button-change-theme' @click='openCloseMenu'>
        <img :src='wallpaper[currentWallpaper]' />Сменить фон
      </button>

    <div :class="[activeMenu ? 'board__theme-wrapper board__theme-wrapper--active' : 'board__theme-wrapper']">
       <div id='wallpapers'>
          <div
          v-for="(item, index) in wallpaper"
          class='wallpapers__item'
          :key="index"
          :style="{ 'background-image': `url(${item})`}"
          @click='changeBackground(index)'
      >
       </div>
    </div>

      <div class='close-wallpapers' @click='openCloseMenu'>
      {{'<'}}
      </div>
  

   
    </div>
   

</div>
</div>

</template>

<style scoped>
    .close-wallpapers{
    display: flex;
    position: fixed;
    top:0;
    height: 100vh;
    width: 35px;
    justify-content: center;
    align-items: center;
    color: black;
    background-color: rgba(255, 255, 255, 0.9);
  }
  .board{
      height: 100%;
      display: flex;
      justify-content: center;
      position: absolute;
      width: 100%;
      left: 0;
      top: 0;
  }
  .wallpapers__item {
      display: inline-block;
      position: relative;
      width: 160px;
      height: 90px;
      background-size: cover;
      margin: 7px;
      border-radius: 0 20px;
      overflow: hidden;
      transition: all 0.5s;
      cursor: pointer;
  }
  .board__theme-wrapper {
      position: fixed;
      display: flex;
      justify-content: end;
      width: 400px;
      height: 100vh;
      background-color: rgba(255, 255, 255, 0.7);
      z-index: 2;
      top: 0;
      left: -400px;
      overflow-y: scroll;
      transition: all 0.4s;
  }
  .board__theme-wrapper--active{
    left: 0px;
  }
  .board__button-change-theme{
    background-color: rgba(255,255,255,0.25);
    color: white;
    align-items: center;
    font-size: 16px;
    border-color: transparent;
    border-radius: 3px;
    min-width: 200px;
    height: 38px;
    cursor: pointer;
    padding: 8px;
    transition: all 0.3s;
    display: flex;
    position: absolute;
    top: 0;
    right: 0;
  }
  .board__button-change-theme img{
    max-width: 50px;
    margin-right: 10px;
  }
  .drop-zone{ 
    background: white;
      height: 150px;
      display: flex;
      align-items: center;
      justify-content: center;
  }
  .drop-zone img{
    max-width: 50px;
    margin: 10px;
  }
  body {
    font-family: "Source Sans Pro", "Arial", sans-serif;
  }
  * {
    box-sizing: border-box;
  }
  .board section{
    width: 30%;
    margin: 5px;
  }
  .todo-list {
    list-style-type: none;
    padding: 10px;
  }
  .done {
    text-decoration: line-through;
    color: #888;
  }
  .new-todo {
    width: 100%;
  }
  .trash-drop {
    border: 2px dashed #ccc !important;
    text-align: center;
    color: #e33;
  }
  .trash-drop:-moz-drag-over {
    border: 2px solid red;
  }
  .todo-item {
    position: relative;
    border: 1px solid #ccc;
    border-radius: 2px;
    padding: 14px 8px;
    margin-bottom: 3px;
    background-color: #fff;
    box-shadow: 1px 2px 2px #ccc;
    font-size: 22px;
    color: black;
  }
  .remove-item {
    float: right;
    color: #a45;
    opacity: 0.5;
    cursor: pointer;
    position: absolute;
    top: 0;
    right: 0;
    display: inline;
    height: 20px;
    width: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .remove-item:hover{
    opacity: 1;
  }
  .board {
    display: flex;
  }
  .board__column{
    background-color: #ededed;
    text-align: center;
    min-width: 100%;
    min-height: 80vh;
  }
  .board__column--in-stock{
    width: 30%;
    min-width: 300px;
  }
  .shoping__img{
    max-width: 50px;
    margin-right: 20px;
  }
  ul{
    list-style: none;
  }
  .shoping__item{
    background-color: white;
    color: black;
    margin: 15px 0;
    padding: 10px;
    border-radius: 15px;
  }
  .shoping__item a{
    display: flex;
    align-items: center;
    color: black;
  }
  .shoping__item:hover{
    box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
  }
  .shoping__title{
    font-size: 24px;
  }
  </style>