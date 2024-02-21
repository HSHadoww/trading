<template>
  <q-page style="background-color:#272727 ; " >
    <q-carousel
      swipeable
      animated
      v-model="slide"
      :autoplay="autoplay"
      ref="carousel"
      infinite
      style="height: calc(100vh - 50px);"
    >
      <q-carousel-slide :name="1" img-src="https://cdn.quasar.dev/img/mountains.jpg" />
      <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg" />
      <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg" />
      <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg" />

      <template v-slot:control>
        <q-carousel-control
          position="top-right"
          :offset="[18, 18]"
          class="text-white rounded-borders"
          style="background: rgba(0, 0, 0, .3); padding: 4px 8px;"
        >
          <q-toggle dense dark color="black" v-model="autoplay" label="Auto Play" />
        </q-carousel-control>

        <q-carousel-control
          position="bottom-right"
          :offset="[18, 18]"
          class="q-gutter-xs"
        >
          <q-btn
            push round dense color="black" text-color="white" icon="arrow_left"
            @click="$refs.carousel.previous()"
          />
          <q-btn
            push round dense color="black" text-color="white" icon="arrow_right"
            @click="$refs.carousel.next()"
          />
        </q-carousel-control>
      </template>
    </q-carousel>
    <q-card class="mb-0 tcol db dbh">
    <div class="row m-0 bg-light" style="height: 100%;">
      <div class="col-lg-6" style="padding: 0;">
        <q-img
          class="rounded-start"
          style="height: 100%;"
          src="https://picsum.photos/1920/1080/?random=10"
        />
      </div>
      <div class="col-lg-6 m-auto text-center flex flex-center" style="padding: 0;">
        <q-card-section>
          <div class="text-h3" style="line-height: 2;">免費教學</div>
          <div class="text-body1" style="line-height: 2; max-width: 600px;">
            是以兩個不願意走出為你他對機關表達有限責任之下女朋友，盯着計算，你怎不來他還培養眼中加入附件從來沒像素較大最高節目治理和我，情形情況一步是怎麼策劃不要收藏網際網路藍色，趨勢她是電信監督維護屏東外掛為。
          </div>

        </q-card-section>
      </div>
    </div>
  </q-card>
  <q-card class="mb-0 tcol db dbh">
    <div class="row m-0 bg-light" style="height: 100%;">
      <div class="col-lg-6 m-auto text-center flex flex-center" style="padding: 0;">
        <q-card-section>
          <div class="text-h3" style="line-height: 2;">問題交流</div>
          <div class="text-body1" style="line-height: 2; max-width: 600px;">
            是以兩個不願意走出為你他對機關表達有限責任之下女朋友，盯着計算，你怎不來他還培養眼中加入附件從來沒像素較大最高節目治理和我，情形情況一步是怎麼策劃不要收藏網際網路藍色，趨勢她是電信監督維護屏東外掛為。
          </div>

        </q-card-section>
      </div>
      <div class="col-lg-6" style="padding: 0;">
        <q-img
          class="rounded-start"
          style="height: 100%;"
          src="https://picsum.photos/1920/1080/?random=10"
        />
      </div>

    </div>
  </q-card>
  <section class="sh">
    <div class="row flex-center tcol"><h3>基礎教學</h3></div>

  <div class="q-pa-md row items-start q-gutter-md flex-center">
    <div class="col-2">
    <q-card class="my-card">
      <img src="https://cdn.quasar.dev/img/mountains.jpg">

      <q-card-section>
        <div class="text-h6 flex flex-center">傳統技術分析(PA)</div>
      </q-card-section>
    </q-card>
    </div>
    <div class="col-2">
    <q-card class="my-card">
      <img src="https://cdn.quasar.dev/img/mountains.jpg">

      <q-card-section>
        <div class="text-h6 flex flex-center">訂單流</div>
      </q-card-section>
    </q-card>
    </div>
    <div class="col-2">
    <q-card class="my-card">
      <img src="https://cdn.quasar.dev/img/mountains.jpg">

      <q-card-section>
        <div class="text-h6 flex flex-center">指標流</div>
      </q-card-section>
    </q-card>
    </div>
    <div class="col-2">
    <q-card class="my-card">
      <img src="https://cdn.quasar.dev/img/mountains.jpg">

      <q-card-section>
        <div class="text-h6 flex flex-center">SMC</div>
      </q-card-section>
    </q-card>
    </div>
  </div>
</section>
<section class="sh db">
  <div class="row flex-center tcol"><h3>為何選擇我們</h3></div>

  <div class="q-pa-md row items-start q-gutter-md flex-center">
    <div class="col-2">
    <q-card class="my-card">
      <img src="https://cdn.quasar.dev/img/mountains.jpg">

      <q-card-section>
        <div class="text-h6 flex flex-center">免費學習</div>
      </q-card-section>
    </q-card>
    </div>
    <div class="col-2">
    <q-card class="my-card">
      <img src="https://cdn.quasar.dev/img/mountains.jpg">

      <q-card-section>
        <div class="text-h6 flex flex-center">問題交流</div>
      </q-card-section>
    </q-card>
    </div><div class="col-2">
    <q-card class="my-card">
      <img src="https://cdn.quasar.dev/img/mountains.jpg">

      <q-card-section>
        <div class="text-h6 flex flex-center">心態引導</div>
      </q-card-section>
    </q-card>
    </div>
  </div>
</section>
  </q-page>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'IndexPage',
  setup () {
    return {
      slide: ref(1),
      autoplay: ref(true),
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
    }
  }
}
</script>
<style>
.tcol{
  color: white;
}
.sh{
  height: 53vh;
}
.db{
  background-color: #1d1d1d;
}
.dbh{
  height: 80vh;
}
</style>
