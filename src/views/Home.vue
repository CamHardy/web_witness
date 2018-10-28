<template>
  <div class="home">
    <div id="container">
      <div id="game">
        <vue-p5
          @setup="setup"
          @draw="draw">
        </vue-p5>
      </div>
    </div>
  </div>
</template>

<script>
  import VueP5 from 'vue-p5'

  export default {
    name: 'home',
    components: {
        "vue-p5": VueP5
    },
    methods: {
        setup(sketch) {
            sketch.createCanvas(sketch.min(0.75*sketch.windowWidth, sketch.windowHeight-42), sketch.min(0.75*sketch.windowWidth, sketch.windowHeight-42));
            sketch.background(33);
        },
        draw(sketch) {
            sketch.fill('#699669');
            sketch.rect(50, 50, 150, 250);
            sketch.fill('#966996');
            sketch.rect(120, 200, 300, 220);
        }
    }
}
</script>

<style>
  canvas {
    display: block;
    margin: auto;
    padding: 0;
  }
</style>
