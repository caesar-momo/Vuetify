<template>
    <div>
        <v-carousel>
            <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
            ></v-carousel-item>
        </v-carousel>
    </div>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://vuetifyjs.com/doc-images/carousel/squirrel.jpg'
          },
          {
            src: 'https://vuetifyjs.com/doc-images/carousel/sky.jpg'
          },
          {
            src: 'https://vuetifyjs.com/doc-images/carousel/bird.jpg'
          },
          {
            src: 'https://vuetifyjs.com/doc-images/carousel/planet.jpg'
          }
        ]
      }
    }
  }
</script>
