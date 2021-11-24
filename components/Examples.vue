<template>
    <div class="border-t-2 py-4 border-dark-900">

        <div class="flex flex-row justify-between items-center">

            <h2 class="text-2xl font-medium select-none">Опис тестових прикладів виконання програми</h2>
            
            <div class="cursor-pointer" @click="unshow = !unshow">

                <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" v-if="unshow">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v3m0 0v3m0-3h3m-3 0H9m12 0a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>

                <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" v-else>
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2m7-2a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>

            </div>
        </div>

        <div class="py-4 px-2" v-if="!unshow">

            <div class="mt-2">

                <ul class="list-decimal text-xl pl-6 pt-2 select-none">

                    <li class="font-medium pt-1">
                        Перегляд списку бірж
                        <img class="mx-auto my-4" src="@/assets/9.png">
                    </li>

                    <li class="font-medium pt-1">
                        Перегляд торгів на біржі
                        <img class="mx-auto my-4" src="@/assets/10.png">
                    </li>

                    <li class="font-medium pt-1">
                        Придбання акцій на біржі
                        <img class="mx-auto my-4" src="@/assets/11.png">
                    </li>

                    <li class="font-medium pt-1">
                        Перегляд списку придбаних акцій
                        <img class="mx-auto my-4" src="@/assets/12.png">
                    </li>

                    <li class="font-medium pt-1">
                        Перегляд списку усіх компаній
                        <img class="mx-auto my-4" src="@/assets/13.png">
                    </li>
                </ul>

            </div>

        </div>

    </div>
</template>

<script>
export default {
    data() {
        return {
            unshow: true
        }
    }
}
</script>