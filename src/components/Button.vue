<template>
  <button class="btn" :class="classColor">
    <slot></slot>
  </button>
</template>

<script>
const COLORS = {
  primary: "btn--primary",
  secondary: "btn--secondary",
};

const SIZES = {
    sm: 'btn--sm',
    base: '',
    lg: 'btn--lg'
}

export default {
  name: "Button",
  props: {
    color: {
      type: String,
      required: false,
      default: "primary",
    },
    size: {
        type: String,
        required: false,
        default: 'base'
    }
  },
  data() {
    return {};
  },
  methods: {},
  computed: {
    classColor() {
        // SIZES['primary']
        // SIZE.sm 
        const color = COLORS[this.color || "primary"]
        const size = SIZES[this.size || 'base']
      return [color, size].join(' ');
    },
  },
};
</script>

<style scoped>
.btn {
  margin: 0;
  border: none;
  font-size: 1rem; /* 16px */
  padding: 0.5em 0.75em; /* 1em = al tamaño de fuente */
  border-radius: 5px;
}
.btn--primary {
  background: black;
  color: white;
}
.btn--secondary {
  background: white;
  color: black;
}

.btn--sm {
    font-size: .8rem;
}

.btn--lg {
    font-size: 1.5rem;
}
</style>
