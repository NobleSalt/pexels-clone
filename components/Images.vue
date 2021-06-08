<template>
  <div class="w-full flex space-between flex-wrap Images">
    <!-- <div class="Images w-full"> -->
    <ImageColumn :padding="'80.5vh'" />
    <ImageColumn :padding="'70.5vh'" />
    <ImageColumn :padding="'80.5vh'" />
    <!-- <SecondColumn :padding="'85vh'" />
    <ThirdColumn :padding="'85vh'" /> -->
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.Images {
  width: 100%;
  position: relative;
  padding-left: 1rem;
  padding: 1rem 0 1rem 1rem;
  justify-content: space-between;
  left: 0;
  right: 0;
}
</style>
