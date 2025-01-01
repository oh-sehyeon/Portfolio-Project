<template>
  <div 
    ref="lazyElement"
    :class="{'is-visible': isVisible}"
    class="lazy-load-wrapper"
  >
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'LazyLoad',
  
  data() {
    return {
      isVisible: false,  // Track if the element is visible
    };
  },

  mounted() {
    this.lazyLoadObserver();
  },

  methods: {
    lazyLoadObserver() {
      const observer = new IntersectionObserver((entries, observer) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            this.$nextTick(() => {
              this.isVisible = true;
            });
            observer.unobserve(entry.target);
          }
        });
      }, {
        threshold: 0.2,  // Trigger when 20% of the element is visible
      });

      observer.observe(this.$refs.lazyElement);
    },
  }
};
</script>

<style scoped>
.lazy-load-wrapper {
  opacity: 0;
  transform: translateX(-1em);
  transition: all 0.6s ease-in-out;
  pointer-events: none;  /* Optionally, prevent interaction before visible */
}

/* Class to apply when the element is visible */
.lazy-load-wrapper.is-visible {
  opacity: 1;
  transform: translateX(0);
  pointer-events: auto; /* Re-enable interaction once the element is visible */
}
</style>
