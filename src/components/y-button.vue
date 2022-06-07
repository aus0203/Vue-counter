<template>
  <div class="button">
    <p class="symbol">{{symbol}}</p>
  </div>
</template>

<script>

export default{
  props:['symbol']
}

</script>

<style>
.button {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 48px;
  height: 48px;
  border: 1px solid #d2d2d2;
  border-radius: 50px;
  cursor: pointer;
  filter: invert(30%);
}

.button:hover{
  background: #eeeeee;
  border: none;
  transition: 300ms ease-in-out;
}

.symbol{
  font-size: 20px;
}
</style>
