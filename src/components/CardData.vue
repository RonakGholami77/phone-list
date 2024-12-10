<template>
  <div>
    <div class="core">
      <h1>{{ name }}</h1>
      <hr />
      <button id="btn" @click="showDetails">show details</button>
    </div>

    <div class="core" v-show="isShow">
      <div class="item">
        <h2>{{ phone }}</h2>
      </div>
      <div class="item">
        <h2>{{ email }}</h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardData',
  props: ['id', 'name', 'phone', 'email'],
  data: function () {
    return {
      isShow: false,
    }
  },
  methods: {
    showDetails() {
      this.isShow = !this.isShow
    },
  },
}
</script>

<style scoped>
.core {
  display: flex;
  align-items: center;
  flex-direction: column;
}
#btn {
  width: 130px;
  height: 40px;
  background-color: orange;
  color: rgb(188, 18, 182);
  text-shadow: 2px 2px 5px gray;
  font-size: 14px;
  font-weight: 400;
}
#btn,
.item {
  border-radius: 16px;
  border: none;
  box-shadow: 2px 2px 5px rgb(202, 200, 200);
  margin-top: 20px;
}
.item {
  font-size: 24px;
  background-color: aqua;
  width: 270px;
  height: 60px;
  padding: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
}
hr {
  width: 100%;
  height: 2px;
  background-color: orange;
  border: none;
  border-radius: 16px;
}
</style>
