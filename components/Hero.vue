<template>
  <div class="hero">
    <img
      class="hero__img"
      src="https://images.pexels.com/photos/2635817/pexels-photo-2635817.jpeg?auto=compress&amp;crop=focalpoint&amp;cs=tinysrgb&amp;fit=crop&amp;fp-y=0.6&amp;h=500&amp;sharp=20&amp;w=1400"
      srcset="
        https://images.pexels.com/photos/2635817/pexels-photo-2635817.jpeg?auto=compress&amp;crop=focalpoint&amp;cs=tinysrgb&amp;fit=crop&amp;fp-y=0.6&amp;h=500&amp;sharp=20&amp;w=350   350w,
        https://images.pexels.com/photos/2635817/pexels-photo-2635817.jpeg?auto=compress&amp;crop=focalpoint&amp;cs=tinysrgb&amp;fit=crop&amp;fp-y=0.6&amp;h=500&amp;sharp=20&amp;w=500   500w,
        https://images.pexels.com/photos/2635817/pexels-photo-2635817.jpeg?auto=compress&amp;crop=focalpoint&amp;cs=tinysrgb&amp;fit=crop&amp;fp-y=0.6&amp;h=500&amp;sharp=20&amp;w=1000 1000w,
        https://images.pexels.com/photos/2635817/pexels-photo-2635817.jpeg?auto=compress&amp;crop=focalpoint&amp;cs=tinysrgb&amp;fit=crop&amp;fp-y=0.6&amp;h=500&amp;sharp=20&amp;w=1500 1500w,
        https://images.pexels.com/photos/2635817/pexels-photo-2635817.jpeg?auto=compress&amp;crop=focalpoint&amp;cs=tinysrgb&amp;fit=crop&amp;fp-y=0.6&amp;h=500&amp;sharp=20&amp;w=2000 2000w,
        https://images.pexels.com/photos/2635817/pexels-photo-2635817.jpeg?auto=compress&amp;crop=focalpoint&amp;cs=tinysrgb&amp;fit=crop&amp;fp-y=0.6&amp;h=500&amp;sharp=20&amp;w=2500 2500w,
        https://images.pexels.com/photos/2635817/pexels-photo-2635817.jpeg?auto=compress&amp;crop=focalpoint&amp;cs=tinysrgb&amp;fit=crop&amp;fp-y=0.6&amp;h=500&amp;sharp=20&amp;w=3000 3000w,
        https://images.pexels.com/photos/2635817/pexels-photo-2635817.jpeg?auto=compress&amp;crop=focalpoint&amp;cs=tinysrgb&amp;fit=crop&amp;fp-y=0.6&amp;h=500&amp;sharp=20&amp;w=3500 3500w,
        https://images.pexels.com/photos/2635817/pexels-photo-2635817.jpeg?auto=compress&amp;crop=focalpoint&amp;cs=tinysrgb&amp;fit=crop&amp;fp-y=0.6&amp;h=500&amp;sharp=20&amp;w=4000 4000w,
        https://images.pexels.com/photos/2635817/pexels-photo-2635817.jpeg?auto=compress&amp;crop=focalpoint&amp;cs=tinysrgb&amp;fit=crop&amp;fp-y=0.6&amp;h=500&amp;sharp=20&amp;w=5000 5000w
      "
    />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.hero {
  height: 100%;
  // max-height: 500px;
  // min-height: 380px;
  height: 38px;

  &__img {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    z-index: -1;
  }
}
</style>
