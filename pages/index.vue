<template>
  <div class="home" @scroll.prevent="handleScroll">
    <Nav :scrolled="scrolled" @dropped="handleDropped" />
    <NavDrop :drop="drop" />
    <div class="main">
      <tryHero />
      <NavSection />
      <!-- <div class="mainContent"> -->
      <!-- <Section /> -->
      <Images />
      <!-- </div> -->
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Free Stock Photos · Pexels",
      meta: [
        {
          hid: "description",
          name: "description",
          content:
            "Free stock photos and videos you can use everywhere. ✓ High-quality ✓ 100% free ✓ No attribution needed"
        },
        {
          hid: "keywords",
          name: "keywords",
          content: "free stock photos, pexels, free, images"
        }
      ]
    };
  },
  data() {
    return {
      scrolled: false,
      drop: false
    };
  },
  methods: {
    handleScroll() {
      // console.log("Scrolled");
      if (scrollY >= 62) {
        this.scrolled = true;
      } else {
        this.scrolled = false;
        if (this.drop) {
          this.scrolled = true;
          scroll(0, 62);
        }
      }
    },
    handleDropped() {
      this.drop = !this.drop;
    }
  },
  mounted() {
    window.onscroll = this.handleScroll;
    if (this.drop) {
      this.scrolled = true;
      window.scroll(0, 62);
    }
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.home {
  // height: 1000px;
  overflow-x: hidden;
  width: 100%;
  height: 100%;

  .main {
    width: 100%;
    height: 100%;

    &Content {
      padding: 0.5rem 1rem;
    }
  }
}
</style>
