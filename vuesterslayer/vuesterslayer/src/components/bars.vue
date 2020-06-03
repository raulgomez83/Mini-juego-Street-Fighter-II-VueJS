<template>
  <div>
    <div class="hpbars">
      <img src="../assets/ryu.jpeg" alt="ryu" />
      <p class="name">Player</p>
      <div class="red">
        <div class="bar" :style="{ width: playerHp + '%' }"></div>
      </div>
      <img src="../assets/bison.jpeg" alt="bison" />
      <p class="name">Enemy</p>
      <div class="red">
        <div class="bar" :style="{ width: enemyHp + '%' }"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "lifebar",
  props: {
    playerHp: Number,
    enemyHp: Number
  }
};
</script>
<style scoped>
img {
  width: 5rem;
}
.hpbars {
  display: flex;
  flex-direction: column;
  width: 50vw;
  background-color: rgba(255, 255, 255, 0);
}
.red {
  background: red;
}
.bar {
  background: yellow;
  height: 25px;
}
.name {
  width: 10rem;
}
</style>
