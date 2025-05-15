<script setup lang="ts">
    import { NuxtLink, USeparator } from '#components';
    import { ref } from 'vue'
    import { useMediaQuery } from '@vueuse/core'
    const current_step = ref(0)
    const left_array = ref(['<span class="font-semibold text-3xl font-mono">Primera presentación</span>','<span class="font-semibold text-xl">30 de octubre del 2022</span>','<span class="font-semibold text-3xl font-mono">Creación del logo original y caracteristico del grupo</span>','<span class="font-semibold text-xl">25 de enero del 2022</span>','<span class="font-semibold text-3xl font-mono">Presentación en el evento LGBT+ de La Paz BCS</span>','<span class="font-semibold text-xl">17 de diciembre de 2023</span>','<span class="font-semibold text-3xl font-mono">Primera publicación grupal</span>','<span class="font-semibold text-xl">20 de enero del 2024</span>','<span class="font-semibold text-3xl font-mono">Presentación en Arena La Paz</span>','<span class="font-semibold text-xl">9 de mayo del 2025</span>','<span class="font-semibold text-3xl font-mono">Creación de la página web oficial de K-Shine</span>'])
    const left_array_extra = ref(['','Primer cover oficial con coreografía y vestuario original junto con la participación de todos los integrantes activos del grupo, bajo el nombre de <span class="font-bold"> K-shine </span>','','Una de las primeras presentaciones hechas con un promotor de apoyo','','Bailando el cover de Sugar Rush Ride en la competencia "All Star Tournament, utilizando vestuario de cuero diseñados por los mismos integrantes"','','Un objetivo importante cumplido. Era uno de los más grandes sueños del grupo bailar en el carnaval de su ciudad.','','Por el evento de cultura del estado'])
    const right_array = ref(['<span class="font-semibold text-xl">11 de diciembre de 2021</span>','<span class="font-semibold text-3xl font-mono">Debut oficial de K-SHINE</span>','<span class="font-semibold text-xl">16 de enero del 2022</span>','<span class="font-semibold text-3xl font-mono">Presentación grupal en el centro recreativo "ElHuevo"</span>','<span class="font-semibold text-xl">7 de Julio de 2023</span>', '<span class="font-semibold text-3xl font-mono">Presentación en la FrikiPosada</span>','<span class="font-semibold text-xl">18 de diciembre de 2023</span>','<span class="font-semibold text-3xl font-mono">Presentación en el Carnaval La Paz</span>','<span class="font-semibold text-xl">16 de marzo del 2024</span>','<span class="font-semibold text-3xl font-mono">Presentación en el teatro de la ciudad</span>','<span class="font-semibold text-xl">14 de mayo del 2025</span>'])
    const right_array_extra = ref(['Participación como grupo independiente sin nombre','','','','','','Se hizo con la intención de presentar a cada uno de los integrantes del grupo y abrir más el grupo','','Acompañando al evento "PintaBCS"'])

    function slider_change() {
        let real_value = current_step.value * 0.10
    }
    const isSmallScreen = useMediaQuery('(max-width: 639px)')
    const sliderOrientation = computed(() => (isSmallScreen.value ? 'horizontal' : 'vertical'))
    const sliderInverted = computed(() => (isSmallScreen.value ? false : true))
</script>

<template>
    <div id="inicio" class="flex flex-col items-center justify-center py-8 gap-20 overflow-hidden">
        <div id="start" class="flex flex-col items-center gap-10 mt-10">
            <div class="w-fit flex justify-center">
                <div class="flex flex-col w-2/3 max-sm:w-full">
                    <img src="/images/kshine_img.jpg"/>
                    <div class="flex pt-6 gap-2 max-sm:flex-col max-sm:text-center max-sm:items-center max-sm:px-4">
                        <p class="text-4xl font-semibold w-fit text-nowrap pr-3 font-mono text-purple-400 max-sm:text-center">¿Quiénes somos?</p>
                        <div class="font-mono">
                            <p class="text-lg pt-1">
                                K-Shine (o "llave al brillo" por su juego de palabras en inglés) es un grupo de dance cover
                                Kpop conformado por 4 integrantes con una trayectoria de alrededor de 3 años activos.
                                <br>
                                <br>
                                Reconocidos por sus presentaciones en alusión a TXT, llevan un gran camino dentro del mundo
                                del dance cover y se encuentran innovando constantemente su calidad y presentación. 
                            </p>
                            <br>
                            <div>
                                <p class="text-lg">Buscan fomentar la diversión y el gusto por el baile kpop a la comunidad, con un objetivo en mente: </p>
                                <br>
                                <div class="flex justify-center italic">
                                    <p class="text-xl text-purple-400 font-bold">"El baile es divertido y ayuda a sanar y conectar con el alma."</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <USeparator id="members" label="Miembros" class="font-mono font-thin scroll-m-20"></USeparator>
            <div class="flex flex-col items-center">
                <div class="flex flex-col items-center ">
                    <div class="flex flex-nowrap max-w-2/3 bg-purple-200 dark:bg-purple-300 max-sm:max-w-full">
                        <UDrawer>
                            <UButton label="Queila" color="neutral" variant="ghost" class="w-3/5 flex justify-center items-center p-0 rounded-none hover:rounded-4xl hover:scale-90 transition-all duration-500 overflow-hidden">
                                <img src="/images/framed_pictures/queila.png">
                            </UButton>
                            <template #content>
                                <div id="member-card" class="flex flex-col items-center justify-center pb-10">
                                    <p class="text-4xl font-mono font-bold text-center py-6">Queila</p>
                                    <div class="flex justify-center items-center max-sm:flex-col">
                                        <img src="/images/queila.jpg" class="w-1/3 max-h-[500px]">
                                        <div class="font-mono p-4 max-w-1/3 max-sm:max-w-full">
                                            <p>Con una sonrisa que ilumina cualquier sala;</p><br>
                                            <p class="text-sm">
                                                <span class="font-semibold italic">Queila</span> es la chispa del grupo: <br>
                                                carismática, energética y llena de pasión. <br>
                                                Como bailarina principal, deslumbra con precisión <br>
                                                y presencia en cada coreografía. Su amor por la <br>
                                                música y su entrega en el escenario inspiran, <br>
                                                mientras su cercanía la convierte en una amiga <br>
                                                esencial para todas.
                                            </p>
                                            <br>
                                            <p class="font-semibold">✨ Cuando está en escena, algo especial comienza.</p>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </UDrawer>
                        <div color="neutral" variant="ghost" class="w-3/5 flex justify-center items-center p-0 rounded-none transition-all duration-500 overflow-hidden select-none bg-purple-100 dark:bg-purple-400">
                            <img src="/images/framed_pictures/blackbox.png" class="bg-white opacity-0">
                            <p class="absolute text-9xl font-bold text-purple-400 dark:text-purple-800 font-mono max-sm:text-7xl">H</p>
                        </div>
                        <UDrawer>
                            <UButton label="Jenny" color="neutral" variant="ghost" class="w-3/5 flex justify-center items-center p-0 rounded-none hover:rounded-4xl hover:scale-90 transition-all duration-500 overflow-hidden">
                                <img src="/images/framed_pictures/jenny.png">
                            </UButton>
                            <template #content>
                                <div id="member-card" class="flex flex-col items-center justify-center pb-10">
                                    <p class="text-4xl font-mono font-bold text-center py-6">Dylan</p>
                                    <div class="flex justify-center items-center max-sm:flex-col">
                                        <img src="/images/jenny.jpg" class="w-1/3 max-h-[500px]">
                                        <div class="font-mono p-4 max-w-1/3 max-sm:max-w-full">
                                            <p>Con determinación y pasión en cada paso;</p><br>
                                            <p class="text-sm">
                                                <span class="font-semibold italic">Dylan</span> es sinónimo de entrega total: <br>
                                                comprometido, enfocado y siempre en constante <br>
                                                evolución. Su dominio del cuerpo en el baile <br>
                                                impresiona, y su habilidad para el maquillaje <br>
                                                embellece cada presentación. Inspira con <br>
                                                disciplina y eleva el nivel del equipo.
                                            </p>
                                            <br>
                                            <p class="font-semibold">💄 Siempre deja su toque brillante en cada detalle.</p>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </UDrawer>
                        <div color="neutral" variant="ghost" class="w-3/5 flex justify-center items-center p-0 rounded-none transition-all duration-500 overflow-hidden select-none bg-purple-100 dark:bg-purple-400">
                            <img src="/images/framed_pictures/blackbox.png" class="bg-white opacity-0">
                            <p class="absolute text-9xl font-bold text-purple-400 dark:text-purple-800 font-mono max-sm:text-7xl">N</p>
                        </div>
                        <UDrawer>
                            <UButton label="Julio" color="neutral" variant="ghost" class="w-3/5 flex justify-center items-center p-0 rounded-none hover:rounded-4xl hover:scale-90 transition-all duration-500 overflow-hidden">
                                <img src="/images/framed_pictures/julio.png">
                            </UButton>
                            <template #content>
                                <div id="member-card" class="flex flex-col items-center justify-center pb-10">
                                    <p class="text-4xl font-mono font-bold text-center py-6">Julio</p>
                                    <div class="flex justify-center items-center max-sm:flex-col">
                                        <img src="/images/julio.jpg" class="w-1/3 max-h-[500px]">
                                        <div class="font-mono p-4 max-w-1/3 max-sm:max-w-full">
                                            <p>Con energía y compromiso desde el primer paso;</p><br>
                                            <p class="text-sm">
                                                <span class="font-semibold italic">Julio</span> es el alma optimista del equipo: <br>
                                                puntual, dedicado y siempre dispuesto a dar más. <br>
                                                Aprende coreografías con rapidez, y su actitud <br>
                                                positiva transforma cada ensayo en un momento <br>
                                                ameno. Con él, el trabajo en grupo se vuelve más <br>
                                                liviano y lleno de sonrisas sinceras.
                                            </p>
                                            <br>
                                            <p class="font-semibold">😄 Su buena vibra siempre llega primero al ensayo.</p>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </UDrawer>
                    </div>
                    <div class="flex flex-nowrap  max-w-2/3 bg-purple-200 dark:bg-purple-300 max-sm:max-w-full">
                        <div color="neutral" variant="ghost" class="w-3/5 flex justify-center items-center p-0 rounded-none transition-all duration-500 overflow-hidden select-none bg-purple-100 dark:bg-purple-400">
                            <img src="/images/framed_pictures/blackbox.png" class="bg-white opacity-0">
                            <p class="absolute text-9xl font-bold text-purple-400 dark:text-purple-800 font-mono max-sm:text-7xl">S</p>
                        </div>
                        <UDrawer>
                            <UButton label="Melanie" color="neutral" variant="ghost" class="w-3/5 flex justify-center items-center p-0 rounded-none hover:rounded-4xl hover:scale-90 transition-all duration-500 overflow-hidden">
                                <img src="/images/framed_pictures/melanie.png">
                            </UButton>
                            <template #content>
                                <div id="member-card" class="flex flex-col items-center justify-center pb-10">
                                    <p class="text-4xl font-mono font-bold text-center py-6">Annie</p>
                                    <div class="flex justify-center items-center max-sm:flex-col">
                                        <img src="/images/melanie.jpg" class="w-1/3 max-h-[500px]">
                                        <div class="font-mono p-4 max-w-1/3 max-sm:max-w-full">
                                            <p>Con una sensibilidad natural para el ritmo;</p><br>
                                            <p class="text-sm">
                                                <span class="font-semibold italic">Annie</span> destaca como una guía innata: <br>
                                                capta cada compás con precisión, enseña con <br>
                                                claridad y paciencia, y siempre brinda ánimo <br>
                                                al equipo. Su responsabilidad es constante, y su <br>
                                                estilo al vestir refleja una elegancia única. <br>
                                                Annie no solo marca el paso, sino también <br>
                                                el corazón de quienes la rodean.
                                            </p>
                                            <br>
                                            <p class="font-semibold">🎶 Siempre tiene el ritmo y la palabra justa para cada momento.</p>
                                        </div>
                                    </div>
                                </div>      
                            </template>
                        </UDrawer>
                        <div color="neutral" variant="ghost" class="w-3/5 flex justify-center items-center p-0 rounded-none transition-all duration-500 overflow-hidden select-none bg-purple-100 dark:bg-purple-400">
                            <img src="/images/framed_pictures/blackbox.png" class="bg-white opacity-0">
                            <p class="absolute text-9xl font-bold text-purple-400 dark:text-purple-800 font-mono max-sm:text-7xl">I</p>
                        </div>
                        <UDrawer>
                            <UButton label="Karie" color="neutral" variant="ghost" class="w-3/5 flex justify-center items-center p-0 rounded-none hover:rounded-4xl hover:scale-90 transition-all duration-500 overflow-hidden">
                                <img src="/images/framed_pictures/karie.png">
                            </UButton>
                            <template #content>
                                <div id="member-card" class="flex flex-col items-center justify-center pb-10">
                                    <p class="text-4xl font-mono font-bold text-center py-6">Kari</p>
                                    <div class="flex justify-center items-center max-sm:flex-col">
                                        <img src="/images/karie.jpg" class="w-1/3 max-h-[500px]">
                                        <div class="font-mono p-4 max-w-1/3 max-sm:max-w-full">
                                            <p>Con liderazgo natural y calidez maternal;</p><br>
                                            <p class="text-sm">
                                                <span class="font-semibold italic">Kari</span> organiza, apoya y motiva con <br>
                                                dedicación inquebrantable. Siempre está atenta <br>
                                                a los detalles y al bienestar del grupo, <br>
                                                animando a cada uno a dar lo mejor. <br>
                                                Su rapidez para aprender y ejecutar, sumada <br>
                                                a su empatía, la convierten en el corazón <br>
                                                estratégico y emocional del equipo.
                                            </p>
                                            <br>
                                            <p class="font-semibold">🌸 Mamá del grupo, pero también el motor que lo impulsa.</p>
                                        </div>
                                    </div>
                                </div>
                            </template>
                        </UDrawer>
                        <div color="neutral" variant="ghost" class="w-3/5 flex justify-center items-center p-0 rounded-none transition-all duration-500 overflow-hidden select-none bg-purple-100 dark:bg-purple-400">
                            <img src="/images/framed_pictures/blackbox.png" class="bg-white opacity-0">
                            <p class="absolute text-9xl font-bold text-purple-400 dark:text-purple-800 font-mono max-sm:text-7xl">E</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <USeparator id="trajectory" label="Trayectoria" class="font-mono font-thin scroll-mt-20"></USeparator>
        <div class="w-2/3 overflow-hidden lg:h-[500px] flex lg:flex-col justify-center ">
            <div class="flex max-sm:flex-col items-center lg:min-h-[400px] lg:gap-5">
                <div class="w-full flex flex-col items-center">
                    <transition name="fade" mode="out-in">
                        <p
                            class="font-mono text-center"
                            v-html="left_array[current_step * 0.10]"
                            :key="left_array[current_step * 0.10]"
                        ></p>
                    </transition>
                    <transition name="fade" mode="out-in">
                        <p
                            class="font-mono text-center"
                            v-html="left_array_extra[current_step * 0.10]"
                            :key="left_array_extra[current_step * 0.10]"
                        ></p>
                    </transition>
                </div>
                <div class="lg:h-full max-sm:h-[100px] max-h-[400px] max-sm:w-full max-sm:px-4">
                    <ClientOnly>
                        <USlider :orientation="sliderOrientation" :inverted="sliderInverted" :step="10" color="neutral" class="h-full" v-model="current_step" :change="slider_change()" />
                    </ClientOnly>
                </div>
                <div class="w-full flex flex-col items-center justify-center">
                    <transition name="fade" mode="out-in">
                        <p
                            class="font-mono text-center"
                            v-html="right_array[Math.floor(current_step * 0.10)]"
                            :key="right_array[current_step * 0.10]"
                        ></p>
                    </transition>
                    <transition name="fade" mode="out-in">
                        <p
                            class="font-mono text-center"
                            v-html="right_array_extra[current_step * 0.10]"
                            :key="right_array_extra[current_step * 0.10]"
                        ></p>
                    </transition>
                </div>
            </div>
        </div>
        <USeparator id="photos" label="Fotos" class="font-mono font-thin scroll-mt-20"></USeparator>
        <div class="flex flex-col items-center lg:max-w-2/3 overflow-hidden mb-12">
            <div class="flex flex-col">
                <img src="/images/general/group_05.png" class="bg-white w-full">
                <div class="flex">
                    <div class="flex flex-col">
                        <img src="/images/general/poster_02.png" class="bg-white w-[380px]">
                        <img src="/images/general/poster_03.png" class="bg-white w-[380px]">
                    </div>
                    <div>
                        <img src="/images/general/poster_01.png" class="bg-white w-full h-full">
                    </div>
                </div>
                <div class="flex flex-col">
                    <img src="/images/general/group_06.png" class="bg-white w-full">
                </div>
            </div>
        </div>
        <div id="networks" class="flex flex-col items-center  w-1/6 fixed bottom-2">
            <div class="flex justify-center items-center bg-purple-100 rounded-xl flex-col gap-0 m-0">
                <div class="flex justify-center items-center p-0 m-0">
                    <a href="https://www.facebook.com/profile.php?id=100089308399149" target="_blank" rel="noopener noreferrer">
                        <UButton icon="ic:baseline-facebook" class="text-4xl bg-transparent text-purple-600 hover:bg-purple-300 transition-all duration-300"></UButton>
                    </a>
                    <a href="https://www.tiktok.com/@kshine.official?fbclid=IwY2xjawJ_UtlleHRuA2FlbQIxMABicmlkETFMNDNXVG1iTHJSWURkS3hxAR6XgvAab0yxMSzxDkCZdX47WedhovZBVqZxc6LPkWHP_Oub-mO3HQFUSqqaRg_aem_4IGr6O9HL5JuY7gx8qqKWA" target="_blank" rel="noopener noreferrer">
                        <UButton icon="iconoir:tiktok-solid" class="text-4xl bg-transparent text-purple-600 hover:bg-purple-300 transition-all duration-300"></UButton>
                    </a>
                    <a href="https://www.instagram.com/kshine.official/reels/" target="_blank" rel="noopener noreferrer">
                        <UButton icon="ri:instagram-fill" class="text-4xl bg-transparent text-purple-600 hover:bg-purple-300 transition-all duration-300"></UButton>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
    .fade-enter-active, .fade-leave-active {
        transition: opacity 0.3s ease;
    }
    .fade-enter-from, .fade-leave-to {
        opacity: 0;
    }
</style>