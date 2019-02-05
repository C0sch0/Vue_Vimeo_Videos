<template>
  <div class="card">
    <div class="card-wrap">
      <div class="card-header">
        <h2 class="card-title"></h2><!-- /.card-title -->
      </div><!-- /.card-header -->
      <div class="card-content">
        <ul v-show-slide:300:ease-in="featuresOpen"
                class="features">

          <p>FINTUAL es una Administradora General de Fondos regulada por la Comisión para el Mercado Financiero (ex SVS) a quien reportamos todos los días el patrimonio de los fondos y nuestros estados financieros trimestralmente.</p>
          <div style="padding:56.25% 0 0 0;position:relative;">
            <iframe ref="video" :id="video" :src="id" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
          </div>
        </ul><!-- /.features -->
        <button
          @click="toggleFeatures"
          class="toggle-features">{{ featuresOpen ? 'Ya, ya, ya entendí' : 'Quiero saber más' }}</button><!-- /.toggle-features -->
      </div><!-- /.card-content -->
    </div><!-- /.card-wrap -->
  </div><!-- /.card -->
</template>

<script>
export default {
  name: 'Video_Collapsable',
  props: {
    id: {required:true},
    video: {required: true},
  }
  ,
  data () {
    return {
      featuresOpen: false
    }
  },
  methods: {
    toggleFeatures () {
      this.featuresOpen = !this.featuresOpen;
      const iframe = this.$refs.video;
      if (this.featuresOpen) {
        iframe.contentWindow.postMessage(JSON.stringify({ method: 'play' }), '*');}
      else {
        iframe.contentWindow.postMessage(JSON.stringify({ method: 'pause' }), '*');}
    }
  }
}
</script>
