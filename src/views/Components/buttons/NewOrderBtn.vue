<template>
  <router-link
    to="/new_order"
    class="new-order-btn btn btn-yellow d-flex align-items-center"
  >
    <div :class="`new-order-btn__icon ${nav ? 'mr-0 mr-md-3' : 'mr-3'}`">
      <svg
        width="12"
        height="12"
        viewBox="0 0 12 12"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <rect
          x="0.0407715"
          y="5.1723"
          width="11.0765"
          height="1.47687"
          fill="#3E392A"
        />
        <rect
          x="6.3175"
          y="0.372437"
          width="11.0765"
          height="1.47687"
          transform="rotate(90 6.3175 0.372437)"
          fill="#3E392A"
        />
      </svg>
    </div>
    <span :class="`new-order-btn__label ${nav ? 'd-md-block d-none' : ''}`"
      >Новый заказ</span
    >
  </router-link>
</template>

<script>
export default {
  props: {
    nav: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.new-order-btn {
  padding: 9px 7px;
}

.new-order-btn:hover{
  transform: none;;
}
</style>
