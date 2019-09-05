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
           <iframe id="googleMap" src="https://www.google.com/maps/d/embed?mid=1efoj3MYRdsJb7c5cfSwf8OXcMtIf6K1d" style="border:0; width: 80vw; height: 80vh"></iframe>
          </lazy-component>
        </no-ssr>
      </div>
      <br>
      <p class="body-2">
        ご意見・ご要望は右下のチャットアイコンから受け付けています。
      </p>
      <!-- Small Chat -->
      <script src="https://embed.small.chat/TMFDLQ4EMGMABU5QUT.js" async></script>
    </v-flex>
  </v-layout>
</template>
<!--
<script>
export default {
}
</script>
<style lang="scss" scoped>

</style>-->