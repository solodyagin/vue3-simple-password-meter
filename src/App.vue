<script lang="ts" setup>
import { ref, type Ref } from 'vue'
import PasswordMeter from './PasswordMeter.vue'

const password: Ref<string> = ref('')

const onScore = (score: { score: number; strength: string }) => {
  console.log(score)
}
</script>

<template>
  <input type="password" v-model="password" />
  <PasswordMeter :password="password" @score="onScore" />
</template>
