<script setup lang="ts">
    import type { NavigationMenuItem } from '@nuxt/ui';

    const items = [
    {
        label: 'Inicio',
        icon: 'material-symbols:family-home-rounded'
    },
    {
        label: 'Covers',
        icon: 'material-symbols:hangout-video'
    },
    {
        label: 'Fotos',
        icon: 'material-symbols:photo-camera-back-rounded',
        slot: 'components' as const
    },
    {
        label: 'Trayectoria',
        icon: 'material-symbols:history',
        slot: 'components' as const
    },
    {
        label: 'Redes',
        icon: 'material-symbols:nest-heat-link-gen-3',
        slot: 'components' as const
    },
    ] satisfies NavigationMenuItem[]

    const colorMode = useColorMode()

    const isDark = computed({
    get() {
        return colorMode.value === 'dark'
    },
    set(_isDark) {
        colorMode.preference = _isDark ? 'dark' : 'light'
    }
    })
</script>

<template>
  <UApp>
    <NuxtRouteAnnouncer />
    <div class="flex justify-between items-center px-10 border-b-1 border-gray-300 shadow-xs">
      <p class="w-fit text-nowrap font-semibold select-none">K-Shine</p>
      <UNavigationMenu :items="items" class="w-full justify-center items-center"/>
      <ClientOnly v-if="!colorMode?.forced">
        <UButton
        :icon="isDark ? 'i-lucide-moon' : 'i-lucide-sun'"
        color="neutral"
        variant="ghost"
        class="text-xl"
        @click="isDark = !isDark"
        />
        <template #fallback>
          <div class="size-8" />
        </template>
      </ClientOnly>
    </div>
    <NuxtPage/>
  </UApp>
</template>
