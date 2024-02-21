<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar style="background: black ;">

        <q-toolbar-title>
          <q-btn flat stretch style="color: white" @click="goToIndex">trading</q-btn>
        </q-toolbar-title>
        <q-btn-group stretch flat>
          <q-btn style="color: white" @click="goToTeach">教學專區</q-btn>
          <q-btn style="color: white" @click="goToChat">交流專區</q-btn>
          <q-btn style="color: white" @click="goToAbout">關於我們</q-btn>
          <q-btn style="color: white" @click="showDialog = true">註冊/登入</q-btn>
        </q-btn-group>
        <q-dialog v-model="showDialog" >
          <q-card>
            <q-card style="background-color: #272727;">
            <q-card-section >

              <q-tabs
                v-model="tab"
                dense
                align="justify"
                class="bg-1d text-white shadow-2"
                :breakpoint="0"
              >
                <q-tab name="login" label="登入" />
                <q-tab name="signin" label="註冊" />
              </q-tabs>
            </q-card-section>
            <q-card-section>
              <div class="text-subtitle2 text-white">這是一個卡片內容</div>
            </q-card-section>
            <q-card-actions>
              <q-btn flat color="white" label="確定" v-close-popup />
              <q-btn flat color="white" label="取消" v-close-popup />
            </q-card-actions>
          </q-card>

          </q-card>
        </q-dialog>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import { useRouter } from 'vue-router'

export default defineComponent({
  name: 'MainLayout',

  setup () {
    const showDialog = ref(false)
    const router = useRouter()

    const goToTeach = () => {
      router.push('/teach')
    }
    const goToIndex = () => {
      router.push('/')
    }
    const goToChat = () => {
      router.push('/chat')
    }
    const goToAbout = () => {
      router.push('/about')
    }

    return {
      showDialog,
      goToTeach,
      goToIndex,
      goToChat,
      goToAbout,
      tab: ref('mails'),
      toggleLeftDrawer () {
        showDialog.value = !showDialog.value
      }
    }
  }
})
</script>

<style>
::-webkit-scrollbar {
  display: none;
}
.bg-1d {
  background-color: #1d1d1d;
}

</style>
