<script setup lang="ts">
defineOptions({
  name: 'IndexPage',
})
const user = useUserStore()
const anyMyrKi = $ref(user.savedMyrKi)

const router = useRouter()
function go() {
  if (anyMyrKi) {
    router.push(`/myrKiSs/${encodeURIComponent(anyMyrKi)}`)
    user.setNewMyrKi(anyMyrKi)
  }
}

const { t } = useI18n()
</script>

<template>
  <div>
    <div py-4 />

    <TheInput
      v-model="anyMyrKi"
      placeholder="enter passcode..."
      autocomplete="false"
      @keydown.enter="go"
    />
    <label class="hidden" for="input">P4SSC0DE REQU1R3D 4 ENTRY</label>

    <div>
      <button
        m-3 text-sm btn
        :disabled="!anyMyrKi"
        @click="go"
      >
        {{ t('button.go') }}
      </button>
    </div>
    <img alt="Myriad Central Node logo" :src="isDark ? '/OBAOLG_DARK_LOGO.png' : '/OBAOLG_LIGHT_LOGO.png'">
    <p>
      <em text-sm opacity-75>You are currently at OBAOLG Central Node within the Myriad Ecosystem, CG SubDivision, if you stumbled here by mistake, you're best bet is to head over to <a href="https://myriad-central.netlify.app">Myriad Central</a> and check the docs for an introduction (this is a BUILDERS site and basic infrastructure familiarity is ASSUMED)</em>
    </p>
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>

<style>
img {
  max-width: 100%;
  height: auto;
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 0px;
  margin-bottom: 20px;
}
</style>
