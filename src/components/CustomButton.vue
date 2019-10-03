<template>
  <div class="button uom-font" @click="$emit('click')">
    <slot></slot>
  </div>
</template>

<script>
export default {
};
</script>

<style lang="scss" scoped>
.button {
  $width: 350px;
  $height: 100px;

  width: $width;
  height: $height;

  &:hover {
    color: black;
    width: $width + 15px;
    background-color: $primary;
  }

  border-color: $primary;
  border-radius: 5px;
  border-width: 5px;
  border-style: solid;

  background-color: rgba(0,0,0,0);

  margin: auto;

  color: white;
  font-size: 45px;
  font-weight: 700;
  user-select: none;
  cursor: pointer;
  text-align: center;

  line-height: $height;
  vertical-align: middle;

  transition: 0.2s;

  max-width: 100%;
}

</style>
