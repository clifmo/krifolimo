<script setup lang="ts">
import { useUserStore } from '~/stores/user'

const props = defineProps<{ name: string }>()
const router = useRouter()
const user = useUserStore()
const { t } = useI18n()
</script>

<template>
  <div>
    <p class="text-4xl">
      <mdi:counter class="inline-block" />
    </p>
    <p>
      {{ t('counter.title') }}
    </p>

    <p class="text-sm opacity-50">
      <em>{{ t('counter.desc') }}</em>
    </p>

    <counter class="text-xl"></counter>

    <div>
      <button class="btn m-3 text-sm mt-6" @click="router.back()">
        {{ t('button.back') }}
      </button>
    </div>
  </div>
</template>
