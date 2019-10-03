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
  $size: 400px;

  width: $size;
  height: $size;
  margin: 25px;
  padding: 20px;

  max-width: 100%;

  background-color: $primary;
  border: $primary 5px solid;
  border-radius: 15px;

  transition: 0.2s;

  position: relative;
  display: table;

  .title {
    color: black;
    width: 100%;
    height: 100%;
    font-size: 60px;
    margin: 0;
    display: table-cell;
    vertical-align: middle;
    text-align: center;

    text-decoration: underline;

    transition: 0.2s;
  }

  .text {
    width: calc(100% - 40px);
    height: 100%;

    position: absolute;
    top: 0;
    left: 0;

    margin: 0;

    padding: 20px;

    opacity: 0;
    transition: 0.2s;
    font-size: 30px;

    display: table-cell;
    vertical-align: middle;
  }

  &:hover {
    background-color: rgba(0,0,0,0);

    .title {
      opacity: 0;
    }

    .text {
      opacity: 1;
    }
  }
}
</style>
