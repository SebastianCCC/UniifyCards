<script setup>
//import packages
import axios from 'axios'
import { ref } from 'vue'
//import components
import Card from '../components/Card.vue'
import CardTitle from '../components/CardTitle.vue'
import CardValue from '../components/CardValue.vue'

//fetch data
const cards = ref([])
const api = 'http://localhost:8000'
axios(`${api}/cards`)
  .then((res) => {
    cards.value = res.data
    console.log(cards)
  })
  .catch((err) => {
    console.log(err)
  })
</script>

<template>
  <section class="flex">
    <template v-for="card in cards" :key="card.id">
      <Card :CardStyle="card.style.class" v-if="card.type == 'card'">
        <CardTitle :CardTitle="card.content.title" />
        <CardValue :CardValue="card.content.value" />
      </Card>
    </template>
  </section>
</template>
