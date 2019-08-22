<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex
      xs12
      sm8
      md6
    >
      <!-- MyMapの埋め込み -->
      <div v-if="$vuetify.breakpoint.xs">
        <no-ssr>
          <lazy-component>
            <iframe id="googleMap" src="https://www.google.com/maps/d/embed?mid=1efoj3MYRdsJb7c5cfSwf8OXcMtIf6K1d" width="100%" height="480"></iframe>
          </lazy-component>
        </no-ssr>
      </div>
      <div v-else>
        <no-ssr>
          <lazy-component>
           <iframe id="googleMap" src="https://www.google.com/maps/d/embed?mid=1efoj3MYRdsJb7c5cfSwf8OXcMtIf6K1d" width="700" height="550"></iframe>
          </lazy-component>
        </no-ssr>
      </div>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  // components: {
  //   Logo,
  //   VuetifyLogo
  // }
}
</script>
<style lang="scss" scoped>

</style>