<template>
  <div>
    <button>
      <slot />
    </button>
  </div>
</template>
<script lang="ts">
export default {
  inheritAttrs: false, //不再继承默认属性
  props: {},
  setup(props, context) {
    const { size, ...rest } = context.attrs;
    return { size, rest };
  },
};
</script>
