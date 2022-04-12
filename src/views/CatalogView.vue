<template>
  <div class="about">
    <h1>Вы находитесь на странице каталог</h1>
    <ul>
      <li v-for="component in components" :key="component.id">
        <router-link exact :to="{path: 'item/' + component.id, query:{name: component.name, img: component.img, price: component.price}}">
          <img :src="component.img" >
          {{component.name}}
        </router-link>
      </li>
    </ul>
  </div>
</template>
<script>
  export default {
    data(){
      return{
        components: [
          {
            id: 1,
            name: 'CPU',
            img: require('../img/cpu.jpg'),
            price: 1600
          },{
            id: 2,
            name: 'Видеокарты',
            img: require('../img/videoCards.jpg'),
            price: 1700
          },{
            id: 3,
            name: 'RAM',
            img: require('../img/ram.jpg'),
            price: 1800
          },{
            id: 4,
            name: 'Блоки питания',
            img: require('../img/powerSupplies.jpg'),
            price: 1900
          },{
            id: 5,
            name: 'SSD drives',
            img: require('../img/ssd.jpg'),
            price: 2000
          },{
            id: 6,
            name: 'HDD hard drives',
            img: require('../img/hdd.jpg'),
            price: 2100
          },{
            id: 7,
            name: 'Материнские платы',
            img: require('../img/motherboard.jpg'),
            price: 2200
          },
        ]
      };
    },
    methods:{

    }
  };
</script>
