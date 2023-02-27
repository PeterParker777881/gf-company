<template>
  <div class="search">
    <img class="glass" src="@/assets/images/search/glass.svg">
    <input class="input" type="text" label="Поиск">
    <img class="cancel" src="@/assets/images/search/cancel.svg">
  </div>
</template>

<style lang="scss">
.search {
  padding: 13px 12px;
  background: #fff;
  border-radius: 8px;
  position: relative;
  width: 288px;
  height: 50px;
}
.glass {
  width: 24px;
  height: 24px;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  left: 12px;
}
.input {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
  padding: 0 48px;
  background: transparent;
  border: none;
  z-index: 1;
}
.cancel {
  width: 12px;
  height: 12px;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  right: 19px;
  cursor: pointer;
  z-index: 2;
}
</style>
