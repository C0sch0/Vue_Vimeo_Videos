<template>
  <div id="row">
    <img alt="Vue logo" src="./assets/logo.png">

    <div>
    <h2 class="card-title">¿Qué es un robot advisor ?</h2>
      <Video_Collapsable
              id='https://player.vimeo.com/video/314101620?title=0&byline=0&portrait=0'
              video="2"
      ></Video_Collapsable>
    </div>

    <div id="video2">
    <h2 class="card-title">¿Se puede invertir más de una vez?</h2>
      <Video_Collapsable
              id='https://player.vimeo.com/video/312786602?title=0&byline=0&portrait=0'
              video="3"
      ></Video_Collapsable>
    </div>

    <div id="video3">
    <h2 class="card-title">¿Qué es y por qué me conviene el APV?</h2>
      <Video_Collapsable id='https://player.vimeo.com/video/312786579?title=0&byline=0&portrait=0'
                         video="4"
      ></Video_Collapsable>
    </div>

    <div id="video4">
    <h2 class="card-title">¿Es seguro Fintual?</h2>
      <Video_Collapsable id='https://player.vimeo.com/video/312786255?title=0&byline=0&portrait=0'
                         video="5"
      ></Video_Collapsable>
    </div>

    <div id="video5">
    <h2 class="card-title">¿Qué pasa si me muero?</h2>
      <Video_Collapsable id='https://player.vimeo.com/video/312786112?title=0&byline=0&portrait=0'
                         video="6"
      ></Video_Collapsable>
    </div>

    <div id="video6">
    <h2 class="card-title">¿Qué es Fintual?</h2>
    <Video_Collapsable id='https://player.vimeo.com/video/312785998?title=0&byline=0&portrait=0'
                       video="7"
    ></Video_Collapsable>
    </div>

  </div>
</template>

<script>
import Video_Collapsable from './components/Video_Collapsable.vue'

export default {
  name: 'app',
  components: {
    Video_Collapsable
  }
}
</script>

<style lang="scss">

#row {
  text-align: center;
  margin-top: 60px;
}

.container {
  margin: 30px 100px;
}
.navbar {
  background-color: white;
  margin-bottom: 32px;
}
input.highcharts-range-selector {
  height: 32px !important;
}

@media (max-width: 768px) {
  .container {
    margin: 10px 20px;
  }
}

html {
  box-sizing: border-box;
  -ms-overflow-style: scrollbar;
}

*,
*::before,
*::after {
  box-sizing: inherit;
}

body {
  background-color: #f4f7fd;
}

.container {
  margin: 0 auto;
  max-width: 1000px;
  padding: 0 15px;
}

.row {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: flex-start;
  margin-left: -15px;
  margin-right: -15px;
}

.card {
  width: 100%;
  padding: 0 15px;
  margin-top: 15px;

  @media screen and (min-width: 992px) {
    width: 50%;
    margin-top: 0;
  }

  .card-wrap {
    background-color: #fff;
    border-radius: 3px;
    box-shadow: 0 0 15px rgba(#1e2f43, 0.15);
    text-align: center;
    padding: 30px 20px;
  }

  .card-title {
    margin: 0;
    font-family: sans-serif;
  }

  .features {
    padding: 0;
    margin: 0;
    list-style: none;

    li {
      margin-top: 10px;
    }
  }

.toggle-features {
  border: 0;
  border-radius: 40px;
  cursor: pointer;
  display: inline-block;
  font-family: sans-serif;
  font-size: 16px;
  padding: 15px 30px;
  text-align: center;
  text-decoration: none;
  transition: background-color 0.3s, box-shadow 0.3s, color 0.3s;
  background-color: #00a3ff;
  color: #fff;
  margin-top: 15px;

  &:hover {
    background-color: darken(#00a3ff, 10%);
  }
}
}
</style>
