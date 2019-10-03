<template>
  <div class="info">
    <h1 class="title uom-font"><slot name="title"></slot></h1>
    <p class="text"><slot></slot></p>
  </div>
</template>

<script>
export default {
};
</script>

<style lang="scss" scoped>
.info {
  width: 400px;
  height: 550px;
  margin: 25px;

  max-width: 100%;

  background-color: rgba(0,0,0,0);
  border: $primary 5px solid;
  border-radius: 15px;

  position: relative;

  .title {
    color: black;

    width: 100%;
    font-size: 50px;
    margin: 0;
    text-align: center;

    padding: 20px 0;

    text-decoration: underline;

    background-color: $primary;
  }

  .text {
    width: calc(100% - 40px);
    height: 100%;

    top: 0;
    left: 0;

    margin: 0;

    padding: 20px;
    font-size: 30px;

    ul {
      margin-top: 5px;
    }
  }
}
</style>
