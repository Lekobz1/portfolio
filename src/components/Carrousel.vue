<template>
    <div class="carousel-container" :style="{transform: 'rotateY(' + rotation + 'deg)'}">
      <div v-for="(subject, index) in subjects" :key="index" class="carousel-item" :class="{selected: selectedIndex === index}" @click="selectSubject(index)">
        {{ subject }}
      </div>
    </div>
  </template>
  
  <script>
export default {
  name: 'Carrousel',
  props: {
    subjects: Array,
    selected: String
  },
  data() {
    return {
      selectedIndex: this.subjects.indexOf(this.selected),
      rotation: 0
    };
  },
  methods: {
    selectSubject(index) {
      this.selectedIndex = index;
      this.$emit('update:selected', this.subjects[index]);
    },
    rotateCarousel() {
      this.rotation += 120;
      if (this.rotation >= 360) {
        this.rotation = 0;
      }
      setTimeout(this.rotateCarousel, 5000);
    }
  },
  mounted() {
    this.rotateCarousel();
  }
};
</script>

<style scoped>
.carousel-container {
  width: 100%;
  height: 400px;
  perspective: 1000px;
  transform-style: preserve-3d;
  transition: transform 1s;
}

.carousel-item {
  width: 200px;
  height: 200px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%) rotateY(0deg) translateZ(200px);
  background-color: #f1f1f1;
  text-align: center;
  line-height: 200px;
  font-size: 24px;
  cursor: pointer;
  transition: transform 1s, background-color 0.5s;
}

.carousel-item:hover {
  background-color: #d9d9d9;
}

.carousel-item.selected {
  background-color: #2196F3;
  color: white;
}

.carousel-item:nth-child(1) {
  transform: translate(-50%, -50%) rotateY(0deg) translateZ(200px);
}

.carousel-item:nth-child(2) {
  transform: translate(-50%, -50%) rotateY(120deg) translateZ(200px);
}

.carousel-item:nth-child(3) {
  transform: translate(-50%, -50%) rotateY(240deg) translateZ(200px);
}

</style>