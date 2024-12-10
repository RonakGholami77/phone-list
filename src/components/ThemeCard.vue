<template>
  <div>
    <div id="theme" v-for="friend in friends" :key="friend.id">
      <CardData :id="friend.id" :name="friend.name" :phone="friend.phone" :email="friend.email" />
    </div>
  </div>
</template>

<script>
import CardData from './CardData.vue'
import friends from './data.js'

export default {
  name: 'ThemeCard',
  data: function () {
    return {
      friends,
    }
  },
  components: {
    CardData,
  },
}
</script>

<style>
#theme {
  width: 400px;
  background-color: rgb(239, 237, 237);
  border: none;
  border-radius: 16px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  margin-bottom: 50px;
  padding: 16px;
}
h1 {
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  color: purple;
  font-size: 36px;
  font-weight: 700;
}
h2 {
  color: white;
  font-size: 24px;
  font-weight: 900;
  text-shadow: 2px 2px 5px gray;
}
</style>
