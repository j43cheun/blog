<template>
  <div class="container">
    <section class="section">
      <h1 class="title">
        Photos
      </h1>
    </section>
    <section class="section">
      <div class="columns is-multiline is-gapless">
        <div v-for="(image, index) in images" :key="index" class="column is-mobile is-half-tablet is-one-third-widescreen">
          <b-image :src="image.src" />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data () {
    return {
      images: [
        {
          src: '/photos/seattle_amazon_spheres_exterior.JPG'
        },
        {
          src: '/photos/redmond_construction.JPG'
        },
        {
          src: '/photos/seattle_kerry_park.JPG'
        },
        {
          src: '/photos/uw_suzallo_library.JPG'
        },
        {
          src: '/photos/seattle_museum_of_flight.JPG'
        },
        {
          src: '/photos/glowing_pokeball.JPG'
        },
        {
          src: '/photos/seattle_woodland_park_zoo_bird.JPG'
        },
        {
          src: '/photos/seattle_woodland_park_zoo_red_panda.JPG'
        },
        {
          src: '/photos/vancouver_english_bay.JPG'
        },
        {
          src: '/photos/poo_poo_point_paragliding.JPG'
        },
        {
          src: '/photos/uw_campus_canada_goose.JPG'
        },
        {
          src: '/photos/seattle_king_street_station.JPG'
        },
        {
          src: '/photos/seattle_amazon_spheres_interior.JPG'
        },
        {
          src: '/photos/marymoor_park_canada_goose.JPG'
        },
        {
          src: '/photos/sammamish_river_trail_duck.JPG'
        }
      ]
    }
  }
}
</script>

<style>
</style>
