
<template>
  <div>
    <h1>Calculator</h1>
    <div class="calculator">
      <div class="current">{{ current || 0 }}</div>

      <div class="btn">AC</div>
      <div class="btn">+/-</div>
      <div class="btn">%</div>
      <div class="btn">/</div>

      <div class="btn">7</div>
      <div class="btn">8</div>
      <div class="btn">9</div>
      <div class="btn">x</div>

      <div class="btn">4</div>
      <div class="btn">5</div>
      <div class="btn">6</div>
      <div class="btn">-</div>

      <div class="btn">1</div>
      <div class="btn">2</div>
      <div class="btn">3</div>
      <div class="btn">+</div>

      <div class="btn zero">0</div>
      <div class="btn">,</div>
      <div class="btn">=</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      current: ''
    }
  }
}
</script>

<style>
.calculator {
  margin: 60px auto;
  width: 500px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(50px, auto);
}

.current {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding-right: 80px;
  grid-column: 1/5;
  background-color: #2c3e50;
  color: #f2f2f2;
}

.btn {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: orange;
  color: #2c3e50;
  font-weight: 600;
  border: 1px solid rgba(129, 91, 20, 0.144);
}

.btn:hover {
  cursor: pointer;
  background-color: rgb(148, 106, 27);
  color: #f2f2f2;
}

.zero {
  grid-column: 1/3;
}
</style>
