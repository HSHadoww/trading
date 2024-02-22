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
            <q-card-section>

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
            <q-card-section style="width: 800px;">
              <div class="q-pa-md" style="width: 525px">
                <q-form
                  v-if="tab === 'login'"
                  @submit="onSubmit"
                  @reset="onReset"
                  class="q-gutter-md tw"
                >
                  <q-input
                    filled
                    v-model="account"
                    label="你的帳號 *"
                    lazy-rules
                    dark
                    :rules="[ val => val && val.length > 0 || '請輸入帳號']"
                  />
                  <q-input
                    filled
                    v-model="password"
                    label="你的密碼 *"
                    lazy-rules
                    dark
                    :rules="[ val => val && val.length > 0 || '請輸入密碼']"
                  />
                  <div>
                    <q-btn label="登入" type="submit" color="black"/>
                    <q-btn label="重置" type="reset" color="white" flat class="q-ml-sm" />
                  </div>
                </q-form>
                <q-form
                  v-if="tab === 'signin'"
                  @submit="onSubmit"
                  @reset="onReset"
                  class="q-gutter-md tw"
                >
                    <q-input
                      filled
                      v-model="account"
                      label="你的帳號 *"
                      lazy-rules
                      dark
                      :rules="[ val => val && val.length > 0 || '請輸入帳號']"
                      class="text-white"
                    />
                    <q-input
                      filled
                      v-model="email"
                      label="你的信箱 *"
                      lazy-rules
                      dark
                      :rules="[ val => val && val.length > 0 || '請輸入密碼']"
                    />
                    <q-input
                      filled
                      v-model="password"
                      label="你的密碼 *"
                      lazy-rules
                      dark
                      :rules="[ val => val && val.length > 0 || '請輸入帳號']"
                    />
                    <q-input
                      filled
                      v-model="password"
                      label="再次輸入密碼 *"
                      lazy-rules
                      dark
                      :rules="[ val => val && val.length > 0 || '請輸入密碼']"
                    />
                    <div>
                      <q-btn label="註冊" type="submit" color="black"/>
                      <q-btn label="重置" type="reset" color="white" flat class="q-ml-sm" />
                    </div>
                </q-form>
              </div>
            </q-card-section>
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
import { useQuasar } from 'quasar'

export default defineComponent({
  name: 'MainLayout',

  setup () {
    const showDialog = ref(false)
    const router = useRouter()
    const $q = useQuasar()

    const name = ref(null)
    const age = ref(null)
    const accept = ref(false)

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
      tab: ref('login'),
      name,
      age,
      accept,
      toggleLeftDrawer () {
        showDialog.value = !showDialog.value
      },
      onSubmit () {
        if (accept.value !== true) {
          $q.notify({
            color: 'red-5',
            textColor: 'white',
            icon: 'warning',
            message: 'You need to accept the license and terms first'
          })
        } else {
          $q.notify({
            color: 'green-4',
            textColor: 'white',
            icon: 'cloud_done',
            message: 'Submitted'
          })
        }
      },

      onReset () {
        name.value = null
        age.value = null
        accept.value = false
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
