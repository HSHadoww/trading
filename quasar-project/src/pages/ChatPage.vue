<template>
  <q-page style="background-color: #272727;">
    <q-card class="bg-27">
    <div class="sh">
    <div class="row flex-center tcol"><h3>心態交流</h3></div>
    <div class="q-pa-md row items-start q-gutter-md flex-center">
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">連續虧損如何調適</div>
        </q-card-section>
      </q-card>
      </div>
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">爆倉後該如何</div>
        </q-card-section>
      </q-card>
      </div>
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">連續盈利該如何保持鎮定</div>
        </q-card-section>
      </q-card>
      </div>
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">該如何保持平靜的心</div>
        </q-card-section>
      </q-card>
      </div>
    </div>
  </div>
</q-card>
<q-card class="bg-1d">
    <div class="sh">
    <div class="row flex-center tcol"><h3>技術交流</h3></div>
    <div class="q-pa-md row items-start q-gutter-md flex-center">
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">論PA與SMC的差別</div>
        </q-card-section>
      </q-card>
      </div>
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">這些指標好用嗎?</div>
        </q-card-section>
      </q-card>
      </div>
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">費雪指標參數設置</div>
        </q-card-section>
      </q-card>
      </div>
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">各流派推薦</div>
        </q-card-section>
      </q-card>
      </div>
    </div>
  </div>
</q-card>
<q-card class="bg-27">
    <div class="sh">
    <div class="row flex-center tcol"><h3>社群推廣</h3></div>
    <div class="q-pa-md row items-start q-gutter-md flex-center">
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">DATA</div>
        </q-card-section>
      </q-card>
      </div>
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">加密刺客TOBM</div>
        </q-card-section>
      </q-card>
      </div>
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">SilverBay銀灣</div>
        </q-card-section>
      </q-card>
      </div>
      <div class="col-2">
      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">
        <q-card-section>
          <div class="text-h6 flex flex-center">MaxCrypto</div>
        </q-card-section>
      </q-card>
      </div>
    </div>
  </div>
</q-card>
  </q-page>
</template>
<script>
export default {
  name: 'TeachPage',
  setup () {
    return {
    }
  }
}
</script>
<style>
.my-card:hover {
transform: scale(1.05);  /* 放大卡片 */
transition: transform 0.3s ease-in-out;  /* 添加過渡效果 */
}
.bg-1d{
background-color: #1d1d1d;
}
.bg-27{
background-color: #272727;
}
</style>
