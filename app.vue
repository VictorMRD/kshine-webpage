<script setup lang="ts">
    import type { NavigationMenuItem } from '@nuxt/ui';
    import { useMediaQuery } from '@vueuse/core'

    const items = [
    {
        label: 'Inicio',
        icon: 'material-symbols:family-home-rounded',
        to: '#inicio'
    },
    {
        label: 'Miembros',
        icon: 'vaadin:group',
        to: '#members'
    },
    {
        label: 'Trayectoria',
        icon: 'material-symbols:history',
        slot: 'components' as const,
        to: '#trajectory'
    },
    {
        label: 'Fotos',
        icon: 'heroicons:photo-16-solid',
        slot: 'components' as const,
        to: '#photos'
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

    const checkSmallScreen = useMediaQuery('(max-width: 639px)')
    const collap = computed(() => (checkSmallScreen.value ? true : false))
</script>

<template>
  <UApp>
    <NuxtRouteAnnouncer />
    <div class="flex max-sm:flex-col justify-between items-center px-10 border-b-1 border-gray-300 shadow-xs fixed w-full light:bg-white dark:bg-slate-900 z-10">
      <UButton class="w-fit text-nowrap max-sm:text-2xl font-semibold select-none bg-white dark:text-white dark:hover:bg-slate-900 dark:bg-slate-900 text-black font-mono hover:bg-white" to="#inicio">K-Shine</UButton>
      <UNavigationMenu :items="items" class="lg:w-full lg:justify-center lg:items-center lg:font-mono max-sm:flex-col"/>
      <ClientOnly v-if="!colorMode?.forced && collap != true">
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
