<script>
    import BoardColumn from './board-column.vue'
    export default {
        'name': "Board",
        data() {
            return {
              boards: {

              },
              wallpaper: [
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite1.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite2.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite3.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite4.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite5.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite6.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite7.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite8.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite9.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite10.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite11.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/BlackWhite12.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/1.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/2.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/3.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/4.png",
                "https://klevtsovaelena.github.io/wallpaper/img/5.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/6.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/7.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/8.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/9.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/10.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/11.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/12.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine1.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine2.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine3.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine4.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine5.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine6.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine7.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine8.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine9.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine10.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine11.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Shine12.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter1.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter2.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter3.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter4.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter5.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter6.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter7.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter8.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter9.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter10.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter11.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Winter12.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Fire1.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Fire2.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Fire3.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Fire4.jpg",
                "https://klevtsovaelena.github.io/wallpaper/img/Fire5.jpg",
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
              list: [
                {
                  id: '1',
                  title: 'Купить доски'
                },
                {
                  id: '2',
                  title: 'Нанять строителей'
                },
                {
                  id: '3',
                  title: 'Заплатить за аренду'
                },
              ],
              inprogress: [
                {
                  id: '4',
                  title: 'Закупить инструменты'
                },
              ],
              done: [
                {
                  id: '5',
                  title: 'Рассчитать денежные средства'
                },
              ],
              newTask: null,
            };
        },
        props: ['test'],
        methods: { 
          handlerDragend(event, type){
            console.log('handlerDragend');
            //console.log(event.target.getAttribute('id'));
            //Получить элемент (колонку) на которую нужно переместить задачу
            //elementFromPoint - Функция из чистого JS, для получения его по его координатам.
            //https://developer.mozilla.org/en-US/docs/Web/API/Document/elementFromPoint
            let Element = document.elementFromPoint(event.x, event.y);
            console.log(Element);
            //Условие, при котором мы перехватываеем, момент, 
            //когда пользователь отпускает задачу в верхний белый блок с рукой
            // Отпускаем элемент именно над блоком с классом drop-zone
            if(Element.getAttribute('class') == 'drop-zone'){
                console.log('Элемент опустился над drop-zone')
                //Найти тот самый элемент, который я перетаскиваю
                // 1 - Из Ивента, получим идентификатор элемента
                const id = event.target.getAttribute('id')
                // 2 - Найти элемент из конкретного массива
                // 2.1 - получить массив (list, inprogress или done) в переменную из которого мы перетаскиваем задачу
                let arrayFrom = this[type];
                // 2.2 - Найти в том массиве, задачу которую мы перетаскиваем
                let element = arrayFrom.find(el => el.id == id);
                console.log('element',element)
                // 2.3 - удалить элемент, из массива, из столбца которого мы перетаскиваем
                //Получаем новый отфильтрованный массив, со всеми элементами, кроме того, что мы перетаскиваем
                let filteredNewArray = arrayFrom.filter(el => el.id !== id);
                //Перезаписываем массив из которого удалили элемент
                this[type] = filteredNewArray
                console.log('filteredNewArray',filteredNewArray)
                //Получим имя массива, в который перемещаем задачи
                let arrayTo = Element.getAttribute('name');
                console.log('arrayTo', arrayTo)
                //Получить массив в который переносим элемент и поместим элемент в его начало
                //unshift - функция для добавление элемента в начало массива, противоположность функции push
                this[arrayTo].unshift(element);
            }
          },
          changeBackground(number){
            this.currentWallpaper = number;
            //Принудительно закрываем Меню
            this.activeMenu = false;
          },
          openCloseMenu(){
            //alert('Сработала функция openCloseMenu')
            //Проверить открыто или закрыто сейчас Меню
            if (this.activeMenu) {
              //если перменная в значении true, то меняем на false
              this.activeMenu = false;
            } else {
              //если перменная в значении false, то меняем на true
              this.activeMenu = true;
            }
          },
          addTask(task, columnName){
            //Готовим объект с задачей
            const taskObject = {
              id: Math.random(),
              title: task
            }
            //Пушим в определенную колонку
            this[columnName].push(taskObject)
          }
        },
        //Регистрируем внешний компонент внутри родительского
        components: {
            'board-column': BoardColumn
        }
    }
</script>

<template>
  <div>
    <div class='board' :style="{'background-image': `url(${wallpaper[currentWallpaper]})` }"> 

      <button class='board__button-change-theme' @click='openCloseMenu'>
         <img :src='wallpaper[currentWallpaper]' />
         Сменить фон
      </button>
      

      <div :class="[activeMenu ? 'board__theme-wrapper board__theme-wrapper--active' : 'board__theme-wrapper']">
          <div id='wallpapers'>
            <div 
              v-for="(item, index) in wallpaper"
              class='wallpapers__item'
              :key="index"
              :style="{'background-image': `url(${item})` }"
              @click='changeBackground(index)'
            >
            </div>
          </div>
          <div class='close-wallpapers' @click='openCloseMenu'>
              {{'<'}}
          </div>
      </div>
      <board-column :addTask="addTask" :taskModel="newTask" title='На складе' :items="list" name='list' :handlerDragend='handlerDragend'></board-column>
      <board-column :addTask="addTask" :taskModel="newTask" title='У курьера' :items="inprogress" name='inprogress' :handlerDragend='handlerDragend'></board-column>
      <board-column :addTask="addTask" :taskModel="newTask" title='Доставлено' :items="done" name='done' :handlerDragend='handlerDragend'></board-column>
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
  </style>
  