<template>
  <div class="lg:w-1/3 sm:w-1/2 ImageColumn">
    <!-- <MyImage />
    <MyImage />
    <MyImage />
    <MyImage /> -->
    <MyImage :style="{ maxHeight: padding }" :height="height" />
    <MyImage :style="{ maxHeight: padding }" :height="height" />
    <MyImage :style="{ maxHeight: padding }" :height="height" />
    <MyImage :style="{ maxHeight: padding }" :height="height" />
    <MyImage :style="{ maxHeight: padding }" :height="height" />
    <MyImage :style="{ maxHeight: padding }" :height="height" />
    <MyImage :style="{ maxHeight: padding }" :height="height" />
    <MyImage :style="{ maxHeight: padding }" :height="height" />
    <MyImage :style="{ maxHeight: padding }" :height="height" />
    <MyImage :style="{ maxHeight: padding }" :height="height" />
  </div>
</template>

<script>
export default {
  props: ["padding"],
  data() {
    return {
      height: "700px"
    };
  }
};
</script>

<style lang="scss">
.ImageColumn {
  padding-right: 1rem;
  overflow: auto;

  // :not(:first-child) {
  //   // bottom: 1rem;
  // }
}
</style>
