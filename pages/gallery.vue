<template>
  <div class="container">
    <section class="section">
      <h1 class="title">
        Gallery
      </h1>
    </section>
    <section class="section">
      <div class="columns is-multiline is-gapless">
        <a v-for="(image, index) in images" :key="index" class="column is-mobile is-half-tablet is-one-third-widescreen" @click="launchModal(index)">
          <b-image :src="image.src" />
        </a>
      </div>
    </section>
    <b-modal v-model="isActive">
      <b-image :src="images[activeIndex].src" />
    </b-modal>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isActive: false,
      activeIndex: 0,
      images: [
        {
          src: '/gallery/seattle_amazon_spheres_exterior.JPG'
        },
        {
          src: '/gallery/redmond_construction.JPG'
        },
        {
          src: '/gallery/seattle_kerry_park.JPG'
        },
        {
          src: '/gallery/uw_suzallo_library.JPG'
        },
        {
          src: '/gallery/seattle_museum_of_flight.JPG'
        },
        {
          src: '/gallery/glowing_pokeball.JPG'
        },
        {
          src: '/gallery/seattle_woodland_park_zoo_bird.JPG'
        },
        {
          src: '/gallery/seattle_woodland_park_zoo_red_panda.JPG'
        },
        {
          src: '/gallery/vancouver_english_bay.JPG'
        },
        {
          src: '/gallery/poo_poo_point_paragliding.JPG'
        },
        {
          src: '/gallery/uw_campus_canada_goose.JPG'
        },
        {
          src: '/gallery/seattle_king_street_station.JPG'
        },
        {
          src: '/gallery/seattle_amazon_spheres_interior.JPG'
        },
        {
          src: '/gallery/marymoor_park_canada_goose.JPG'
        },
        {
          src: '/gallery/sammamish_river_trail_duck.JPG'
        }
      ]
    }
  },
  methods: {
    launchModal (activeIndex) {
      this.isActive = true
      this.activeIndex = activeIndex
    }
  }
}
</script>

<style>
a .image img {
  filter: grayscale(100%);
}
a .image img:hover {
  filter: grayscale(0%);
}
</style>
