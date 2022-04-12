<template>
  <div>
    <h1>Вы выбрали товар: {{name}}</h1>
    <img :src="img" alt="name">
    <h2>Цена товара: {{price}}</h2>
    <div class="btn" @click="goBack">Назад</div>
  </div>
</template>

<script>
export default {
  name: "ItemsView",
  data(){
    return{
      id: this.$route.params['id'],
      name: this.$route.query.name,
      img: this.$route.query.img,
      price: this.$route.query.price,
    };
  },
  methods:{
    goBack(){
      this.$router.push('/catalog');
    }
  }
}
</script>

<style scoped>

</style>