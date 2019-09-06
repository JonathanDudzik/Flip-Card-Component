<template>
    <section class="section">
      <div class="container">
        <div class="level">
          <div class="level-item card-stock">
            <div class="card-stock-side" ref="cardSideFront">
              <figure class="image">
                <img src="../assets/Slide1.jpg">
              </figure>
            </div>
            <div class="card-stock-side card-stock-side-back" ref="cardSideBack">
              <figure class="image">
                <img src="../assets/Slide2.jpg">
              </figure>
            </div>
          </div>
        </div>
        <div @click="flip" class="button">CHECK YOUR ANSWER!</div>
      </div>
    </section>
</template>

<script> 
export default { 
  methods: {
    flip() {
      const { cardSideFront, cardSideBack  } = this.$refs
      TweenMax.to(cardSideFront, 1, { ease: Power1.easeOut, rotationY: "+=180deg"})
      TweenMax.to(cardSideBack, 1, { ease: Power1.easeOut, rotationY: "+=180"})
    }
  } 
} 
</script>

<style lang="scss">

  @import "../../node_modules/bulma/sass/utilities/_all.sass";
  @import "../../node_modules/bulma/sass/base/_all.sass";
  @import "../../node_modules/bulma/sass/elements/_all.sass";
  @import "../../node_modules/bulma/sass/components/_all.sass";
  @import "../../node_modules/bulma/sass/layout/_all.sass";
  @import "../../node_modules/bulma/sass/grid/_all.sass";

  .card-stock {
    perspective: 1000px;
    position: relative;
    height: 500px;
  
    &-side {
      width: 100%;
      height: 500px;
      position: absolute;
      top: 0;
      backface-visibility: hidden;

      &-back {
        transform: rotateY(180deg);
      }
    }
  }

</style>