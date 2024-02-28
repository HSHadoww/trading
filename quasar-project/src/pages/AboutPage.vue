<template>
  <q-page style="background-color: #272727;">
    <div class="text-h2" style="color: white;">
      <q-card class="mb-0 tcol db dbh">
      <div class="row m-0 bg-light" style="height: 100%;">
        <div class="col-lg-6" style="padding: 0;">
          <q-img
            class="rounded-start"
            style="height: 100%;"
            src="../assets/a1.jpg"
          />
        </div>
        <div class="col-lg-6 m-auto text-center flex flex-center" style="padding: 0;">
          <q-card-section>
            <div class="text-h3" style="line-height: 2;">關於我們</div>
            <div class="text-body1" style="line-height: 2; max-width: 600px;">
              創立這裡的初衷是為了避免大家在網路上找不到想要的資訊，這裡提供了各種不同的資訊，希望能夠幫助到大家。也是避免某些唯利是圖的人用很基礎的東西卻要收取高額的費用，這裡的資訊都是免費的，希望大家能夠善加利用。
            </div>
          </q-card-section>
        </div>
      </div>
      </q-card>
    </div>
    <div class="tish text-white flex flex-center">
      <h2>常見問題</h2>
    </div>
    <div class="q-pa-md flex flex-center  sh" style="max-width: 100vw">
      <q-list bordered  style="width: 100%;">
        <q-expansion-item
          group="somegroup"
          label="之後會考慮收費制嗎?"
          header-class="bg-1d text-white"
          expand-icon-class="text-white"
          default-opened
        >
          <q-card class="bg-teal-2">
            <q-card-section>
              不會，我們的初衷是為了幫助大家，所以我們不會收取任何費用。
            </q-card-section>
          </q-card>
        </q-expansion-item>

        <q-separator />

        <q-expansion-item
          group="somegroup"
          label="所有種類圖表都合適嗎?"
          header-class="bg-1d text-white"
          expand-icon-class="text-white"
        >
          <q-card class="bg-teal-2">
            <q-card-section>
              基本上PA、指標、訂單流、SMC都是可以的，但是我們會先建議大家從PA開始，因為這是最基礎的。而且每個市場的特性不一樣所以可能會有些許不同。
            </q-card-section>
          </q-card>
        </q-expansion-item>

        <q-separator />

        <q-expansion-item
          group="somegroup"
          label="會有線下聚會嗎?"
          header-class="bg-1d text-white"
          expand-icon-class="text-white"
        >
          <q-card class="bg-teal-2">
            <q-card-section>
              可能會有，但是目前還沒有計畫。也要看大家的參與度如何在做安排。
            </q-card-section>
          </q-card>
        </q-expansion-item>

        <q-separator />

        <q-expansion-item
          group="somegroup"
          label="可以搬運文章嗎?"
          header-class="bg-1d text-white"
          expand-icon-class="text-white"
        >
          <q-card class="bg-teal-2">
            <q-card-section>
              基本上只要通過別人同意就可以，所以要搬運前記得先問過原作者。
            </q-card-section>
          </q-card>
        </q-expansion-item>
        <q-separator />
        <q-expansion-item
          group="somegroup"

          label="交流區推薦的社群可信度高嗎?"
          header-class="bg-1d text-white"
          expand-icon-class="text-white"
        >
          <q-card class="bg-teal-2">
            <q-card-section>
              這我無法保證，但是如果有人待過覺得不行的話，可以在交流區提出來，我們會進行調查。如屬於詐騙社群的話，我們回將其列入黑名單。
            </q-card-section>
          </q-card>
        </q-expansion-item>

        <q-separator />
      </q-list>
    </div>
    <div class="tcol sh1" style="background-color: #1d1d1d;">
    <div class="flex flex-center tish text-white"><h3>聯絡我們</h3></div>
    <div>&nbsp;</div>
    <div class="flex flex-center">
      <q-card style="width: 80%; background-color: #272727;">
      <q-card-section>
        <q-form class="q-gutter-md">
          <q-input
            v-model="inputModel"
            filled
            clearable
            color="purple-12"
            label="暱稱"
            dark
            @keydown="processInputFill"
            @focus="processInputFill"
          />

          <q-input
            v-model="textareaModel"
            filled
            clearable
            autogrow
            color="green-8"
            label="電子信箱"
            dark
            @keydown="processTextareaFill"
            @focus="processTextareaFill"
          />
          <q-select
            outlined
            v-model="model"
            label="問題類型"
            :options="options"
            dark
          />

          <q-input
            v-model="textareaModel"
            filled
            clearable
            type="textarea"
            color="red-12"
            label=" 問題及建議"
            dark
            @keydown="processTextareaFill"
            @focus="processTextareaFill"
          />

          <div class="flex flex-center ">
            <q-btn label="送出" type="submit" color="black"/>
          </div>
        </q-form>
      </q-card-section>
    </q-card>
    </div>
    <div>&nbsp;</div>
  </div>
  </q-page>
</template>
<script>
import { ref } from 'vue'
export default {
  name: 'AboutPage',
  setup () {
    return {
      model: ref(null),
      options: [
        '教學文建議', '交流區建議', '服務品質', '其他'
      ]
    }
  }
}
</script>
<style>
.tish{
  height: 7vh;
}
.sh{
  height: 30vh;
}
.bg-1d{
  background-color: #0a0a0a;
}
.sh1{
  height: 45vh;
}
</style>
