<template>
    <div id="main-container" class="flex flex-col items-center justify-center py-8 gap-20">
        <div id="start" class="flex flex-col gap-20">
            <div class="w-fit flex justify-center ">
                <div class="flex flex-col w-2/3">
                    <img src="../assets/images/kshine_img.jpg"/>
                    <div class="flex pt-6 gap-2">
                        <p class="text-4xl font-semibold w-fit text-nowrap pr-3 font-mono text-purple-400">¿Quiénes somos?</p>
                        <div class="font-mono">
                            <p class="text-lg pt-1">
                                K-Shine (o "llave al brillo" por su juego de palabras en inglés) es un grupo de dance cover
                                Kpop conformado por 4 integrantes con una trayectoria de alrededor de 3 años activos.
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
            <div class="w-full bg-purple-100 flex flex-col items-center overflow-hidden">
                <p class="text-4xl font-semibold py-4 font-mono text-purple-400">Integrantes</p>
                <UDrawer>
                    <UButton label="Queila" color="neutral" variant="ghost" class="w-20 h-20 flex justify-center items-center"/>
                    <template #content>
                        <div id="member-card" class="flex flex-col items-center justify-center pb-10">
                            <p class="text-4xl font-mono font-bold text-center py-6">Queila</p>
                            <div class="flex justify-center">
                                <img src="/assets/images/queila.jpg" class="w-1/5 h-1/5">
                                <div class="font-mono p-4 max-w-1/3">
                                    <p class="">Con una sonrisa que ilumina cualquier sala; </p><br>
                                    <p class="text-sm">
                                        Tiene una energía que contagia a todos a su alrededor,<br>
                                        <span class="font-semibold italic">Queila</span> es el alma alegre y carismática del grupo. <br>
                                        Como bailarina principal, deslumbra en cada coreografía con una mezcla única <br>
                                        de pasión, precisión y presencia escénica. Siempre lista para <br>
                                        brillar junto a sus compañeras, nunca deja pasar una oportunidad <br>
                                        de oro para subirse al escenario y compartir su amor por la música <br> 
                                        con los fans. Su apoyo incondicional y cercanía hacen de ella no <br> 
                                        solo una artista dedicada, sino también una amiga esencial dentro del grupo.
                                    </p> 
                                    <br>
                                    <p class="font-semibold">✨ Cuando ella está en escena, sabes que algo especial está por comenzar.</p>
                                </div>
                            </div>
                        </div>
                        <!-- <Placeholder class="h-48 m-4" /> -->
                    </template>
                </UDrawer>
            </div>
        </div>
        <div id="covers">
            covers
            <div class="w-20 h-20 bg-red-800">
                
            </div>
        </div>
        <div id="photos">
            photos
        </div>
        <div id="trajectory">
            trajectory
        </div>
        <div id="networks">
            networks
        </div>
    </div>
</template>