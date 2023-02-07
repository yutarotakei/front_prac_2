<template>
  <div class="about">
    <h1>This is an about page</h1>
<p class="circle"></p>

<div class="ele-container">
  <div class="ele-wrapper">
    <div class="ele-tail"></div>
    <div class="ele-body">
      <div class="ele-head">
        <div class="ele-eyebrows"></div>
        <div class="ele-eyes"></div>
        <div class="ele-mouth"></div>
        <div class="ele-fang-front"></div>
        <div class="ele-fang-back"></div>
        <div class="ele-ear"></div>
      </div>
    </div>
    <div class="ele-leg-1 ele-leg-back">
      <div class="ele-foot"></div>
    </div>
    <div class="ele-leg-2 ele-leg-front">
      <div class="ele-foot"></div>
    </div>
    <div class="ele-leg-3 ele-leg-back">
      <div class="ele-foot"></div>
    </div>
    <div class="ele-leg-4 ele-leg-front">
      <div class="ele-foot"></div>
    </div>
  </div>
</div>

  <v-sparkline
    :value="value"
    :gradient="gradient"
    :smooth="radius || false"
    :padding="padding"
    :line-width="width"
    :stroke-linecap="lineCap"
    :gradient-direction="gradientDirection"
    :fill="fill"
    :type="type"
    :auto-line-width="autoLineWidth"
    auto-draw
  ></v-sparkline>

<template>
  <v-parallax src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"></v-parallax>
</template>
<template>
  <v-parallax src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"></v-parallax>
</template>


<template>
  <v-sparkline
    :value="value"
    :gradient="gradient"
    :smooth="radius || false"
    :padding="padding"
    :line-width="width"
    :stroke-linecap="lineCap"
    :gradient-direction="gradientDirection"
    :fill="fill"
    :type="type"
    :auto-line-width="autoLineWidth"
    auto-draw
  ></v-sparkline>
</template>

</div>
</template>


<style scoped>
.circle {
   width: 100px;
   height: 100px;
   margin : 50px auto;
   border-radius: 50px;
   background: #ed93b0;
   animation: mochimochi 1s infinite;
}

@keyframes mochimochi {
  0% {
    transform: scale(1, 0.8);
  }
  20% {
    transform: scale(0.8, 1.1);
  }
  90% {
    transform: scale(1, 1);
  }
  100% {
    transform: scale(1, 0.8);
  }
}

   
</style>

<script>
  const gradients = [
    ['#222'],
    ['#42b3f4'],
    ['red', 'orange', 'yellow'],
    ['purple', 'violet'],
    ['#00c6ff', '#F0F', '#FF0'],
    ['#f72047', '#ffd200', '#1feaea'],
  ]

  export default {
    data: () => ({
      width: 2,
      radius: 10,
      padding: 8,
      lineCap: 'round',
      gradient: gradients[5],
      value: [0, 2, 5, 9, 5, 10, 3, 5, 0, 0, 1, 8, 2, 9, 0],
      gradientDirection: 'top',
      gradients,
      fill: false,
      type: 'trend',
      autoLineWidth: false,
    }),
  }
</script>
