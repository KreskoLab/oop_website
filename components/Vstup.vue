<template>
    <div class="border-t-2 py-4 border-dark-900">

        <div class="flex flex-row justify-between items-center">

            <h2 class="text-2xl font-medium select-none">Вступ</h2>
            
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

            <p class="text-xl select-none">
                Необхідно розробити програму для симуляції роботи Фондової біржі. 
                Програма повинна мати наступні функціональні можливості:
            </p>

            <ul class="list-disc text-xl pl-8 pt-2 select-none">
                <li>генерація бірж</li>
                <li>генерація компаній</li>
                <li>генерація трейдерів</li>
                <li>купівля/продаж акцій</li>
                <li>збереження данних бірж, компаній, трейдерів</li>
            </ul>

            <p class="text-xl select-none pt-4">
                Основної функцією буде – купівля/продаж акцій.
            </p>

            <div class="mt-2">
                <img src="@/assets/1.png">
                <p class="text-center text-xl pt-5">Дерево функцій</p>
            </div>   

            <div class="mt-4">

                <p class="text-xl">
                    Основні сутності предметного середовища та їх атрибути:
                </p>

                <div class="flex flex-row justify-between ">

                    <div class="flex flex-col">
                        <ul class="list-disc text-xl pl-8 pt-2 select-none">
                            <li>
                                Біржа
                                <ul class="list-circle pl-8">
                                    <li>назва</li>
                                    <li>код</li>
                                    <li>перелік вимог</li>
                                    <li>коміссія</li>
                                    <li>список компаній</li>
                                    <li>список трейдерів</li>
                                    <li>заявки на продаж</li>
                                    <li>заявки на покупку</li>
                                </ul>
                            </li>

                            <li class="pt-2">
                                Час
                                <ul class="list-circle pl-8">
                                    <li>швидкість</li>
                                    <li>день</li>
                                    <li>місяць</li>
                                    <li>рік</li>
                                    <li>квартал</li>
                                </ul>
                            </li>
                        </ul>
                    </div>

                    <div class="flex flex-col">
                        <ul class="list-disc text-xl pl-8 pt-2 select-none">
                            <li>
                                Компанія
                                <ul class="list-circle pl-8">
                                    <li>назва</li>
                                    <li>сфера діяльності</li>
                                    <li>прибуток</li>
                                    <li>біржа</li>
                                    <li>капіталізація</li>
                                    <li>список компаній</li>
                                    <li>акції</li>
                                </ul>
                            </li>

                            <li class="pt-8">
                                Трейдер
                                <ul class="list-circle pl-8">
                                    <li>ім'я</li>
                                    <li>капітал</li>
                                    <li>дохід</li>
                                    <li>біржа</li>
                                    <li>список акцій</li>
                                </ul>
                            </li>
                        </ul>
                    </div>

                </div>

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