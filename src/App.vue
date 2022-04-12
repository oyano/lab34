<template>
  <div id="app">
    <nav>
      <router-link to="/">Главная</router-link> |
      <router-link to="/catalog">Каталог</router-link>
    </nav>
    <router-view/>
  </div>
</template>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

a {
  font-weight: bold;
  color: #2c3e50;
  transition: all .5s;
}
a:hover{
  color: #42b983;
}
a:hover > img{
  opacity: .7;
}
nav a{
  text-transform: uppercase;
}
a.router-link-exact-active {
  color: #42b983;
}
ul{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  width: 70%;
  margin: 0 auto;
}
li a{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 20px 20px 20px 20px;
}
li::marker{
  content: '';
}
img{
  width: 200px;
  transition: all .5s;
  margin-bottom: 10px;
}
.btn{
  width: 100px;
  height: 40px;

  background: #2c3e50;
  color: white;
  border-radius: 5px;
  border: solid 1px #2c3e50;

  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  position: relative;
  cursor: pointer;
  transition: all .2s;
}
.btn:hover{
  background: #42b983;
  border: solid 1px #42b983;
}
.text{
  display: inline;
  background-color: white;
  border: none;
  color: #42b983;
}
.text:hover{
  background-color: white;
  border: none;
}
.text:after{
  content: '';
  position: absolute;
  transform: translate(-74px,18px);
  width: 0%;
  height: 2px;
  background: #42b983;
  transition: all .2s;
}
.text:hover:after{
  content: '';
  position: absolute;
  transform: translate(-74px,18px);
  width: 100%;
  height: 2px;
  background: #42b983;
  transition: all .2s;
}
</style>
