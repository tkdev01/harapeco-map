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
      <div id="mymapArea"></div>
      <div v-if="$vuetify.breakpoint.xs">
        
        <!--
        <no-ssr>
          <lazy-component>
            <iframe id="googleMap" src="https://www.google.com/maps/d/embed?mid=1efoj3MYRdsJb7c5cfSwf8OXcMtIf6K1d" width="100%" height="480"></iframe>
          </lazy-component>
        </no-ssr>
        -->
      </div>
      <div v-else>
        <!--
        <no-ssr>
          <lazy-component>
           <iframe id="googleMap" src="https://www.google.com/maps/d/embed?mid=1efoj3MYRdsJb7c5cfSwf8OXcMtIf6K1d&ll=," style="border:0; width: 80vw; height: 80vh"></iframe>
          </lazy-component>
        </no-ssr>
        -->
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

<script>
export default {
  data: function(){
    return {
      latitude: 0,
      longitude: 0,
    }
  },
  methods: {
    displayCurrentLocationMap: function() {
      if(navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(function(position){
          this.latitude = position.coords.latitude;
          this.longitude = position.coords.longitude;
          this.readMyMap();
        }.bind(this));
      }
    },
    readMyMap: function() {
      let mapUrl = "https://www.google.com/maps/d/embed?mid=1efoj3MYRdsJb7c5cfSwf8OXcMtIf6K1d";
      if(this.latitude != 0 && this.longitude != 0){ 
        mapUrl += "&ll=";
        mapUrl += this.latitude;
        mapUrl += ",";
        mapUrl += this.longitude;
        mapUrl += "&z=13" // Zoom level 13 = 1km
      }

      let mymapArea = document.getElementById("mymapArea");
      let flameElm = document.createElement("iframe");
      flameElm.id = "googleMap";
      flameElm.src = mapUrl;
      flameElm.style = "border:0; width: 90vw; height: 80vh";
      mymapArea.appendChild(flameElm);
    }
  },
  mounted: function(){
    this.displayCurrentLocationMap();
  }
}

</script>
<!--
<style lang="scss" scoped>
</style>
-->