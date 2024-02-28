<template>
    <q-page style="background-color: #272727;">
      <q-card class="bg-27">
      <div class="sh">
      <div class="row flex-center tcol"><h3>傳統技術分析(PA)</h3></div>
      <div class="q-pa-md row items-start q-gutter-md flex-center">
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">支撐阻力</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">趨勢線</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">斐波那契</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">斐波那契回撤</div>
          </q-card-section>
        </q-card>
        </div>
      </div>
    </div>
  </q-card>
  <q-card class="bg-1d">
      <div class="sh">
      <div class="row flex-center tcol"><h3>指標流</h3></div>
      <div class="q-pa-md row items-start q-gutter-md flex-center">
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">移動平均線 ( MA )</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">KD 指標</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">RSI 指標</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">MACD 指標</div>
          </q-card-section>
        </q-card>
        </div>
      </div>
    </div>
  </q-card>
  <q-card class="bg-27">
      <div class="sh">
      <div class="row flex-center tcol"><h3>訂單流</h3></div>
      <div class="q-pa-md row items-start q-gutter-md flex-center">
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">訂單牆</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">市場深度</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">清算圖</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">盤口</div>
          </q-card-section>
        </q-card>
        </div>
      </div>
    </div>
  </q-card>
  <q-card class="bg-1d">
      <div class="sh">
      <div class="row flex-center tcol"><h3>SMC</h3></div>
      <div class="q-pa-md row items-start q-gutter-md flex-center">
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">訂單塊</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">流動性</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">FVG</div>
          </q-card-section>
        </q-card>
        </div>
        <div class="col-2">
        <q-card class="my-card">
          <img src="https://cdn.quasar.dev/img/mountains.jpg">
          <q-card-section>
            <div class="text-h6 flex flex-center">結構破壞</div>
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
