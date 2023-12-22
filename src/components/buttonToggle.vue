<template>
  <div :onClick="toggle" class="outside" :class="toggled && 'outside-toggled'">
    <div class="inside" :class="toggled && 'inside-toggled'" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      toggled: false,
    };
  },

  methods: {
    toggle() {
      this.toggled = !this.toggled;
      console.log(this.toggled)
    },
  },
};
</script>

<style scoped>
.outside {
  width: 80px;
  height: 50px;
  background-color: #39383c;
  border-radius: 25px;
  position: relative;
  cursor: pointer;
  transition: background-color 0.2s ease-in-out;
  overflow: hidden;
}

.inside {
  width: 40px;
  height: 40px;
  background-color: #fff;
  border-radius: 50%;
  position: absolute;
  top: 5px;
  left: 5px;
  transition: left 0.2s;
  transition-timing-function: cubic-bezier(-1.36e-35, -3.26, 4.26, 1.00);
}

.inside-toggled {
  left: calc(100% - 45px);
}

.outside-toggled {
  background-color: #2FD158;
}
</style>
