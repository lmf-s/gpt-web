<script setup lang='ts'>
import { defineAsyncComponent, ref } from 'vue'
import { UserAvatar } from '@/components/common'

const Setting = defineAsyncComponent(() => import('@/components/common/Setting/index.vue'))
// const state = reactive({
//   clickCount: 0,
// })
const show = ref(false)
// function handleClick() {
//   state.clickCount++

//   if (state.clickCount === 3) {
//     state.clickCount = 0
//     show.value = true
//   }
// }
</script>

<template>
  <footer class="flex items-center justify-between min-w-0 p-4 overflow-hidden border-t dark:border-neutral-800">
    <div class="flex-1 flex-shrink-0 overflow-hidden">
      <UserAvatar />
    </div>

    <!-- <HoverButton>
      <span class="text-xl text-[#4f555e] dark:text-white">
        <SvgIcon icon="ri:settings-4-line" />
      </span>
    </HoverButton> -->

    <Setting v-if="show" v-model:visible="show" />
  </footer>
</template>
