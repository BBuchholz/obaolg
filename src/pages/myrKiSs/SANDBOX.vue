<script setup>
import { ref } from 'vue'

const allCards = ref([
  {
    passCode: 'CLoneME',
    wxrdtype: '',
    localDescription: '',
    uuid: '',
    image: '',
  },
])
</script>

<template>
  <h1>"begIN THA WORKSHOP"</h1>
  <p mt-4 text-sm>
    AL BUILDERS know that the ESSENCE of BUILDING is in DELIVERABLES, so here will be your WORKSHOP for all GUILD PROJECKTS going forward. You will be expected to link each project here for review when ready and in doing so a portfolio of ARTIFACTS will arise... WELLcome 2 THA BAOLG!
  </p>
  <div class="card">
    <img src="/SANDBOX-257e_CARD.png">
  </div>
  <p mt-4 text-sm>
    <span opacity-75>PROJECKT CARDS:</span>
    <ul>
      <li v-for="aCard in allCards" :key="aCard">
        <div>
          <RouterLink :to="`/myrKiSs/${aCard.passCode}`" replace>
            {{ aCard.passCode }}
            <div class="card">
              <img :src="aCard.image">
            </div>
          </RouterLink>
        </div>
      </li>
    </ul>
  </p>
</template>

<style>
  .card {
    max-width: 50%;
    height: auto;
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-top: 50px;
    margin-bottom: 50px;
    border: 5px;
    border-color: white;
    border-style: solid;
    border-radius: 1%;
  }
</style>
