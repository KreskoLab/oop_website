<template>
    <div class="border-t-2 py-4 border-dark-900">

        <div class="flex flex-row justify-between items-center">

            <h2 class="text-2xl font-medium select-none">UML-діаграма прецедентів</h2>
            
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

            <div class="w-full mt-2">
                <img class="mx-auto" src="@/assets/2.png">
                <p class="text-center text-xl pt-5">Діаграма прецедентів</p>
            </div> 

            <div class="mt-6">
                <p class="text-xl font-medium">Основні прецеденти:</p>

                <ul class="list-decimal text-xl pl-6 pt-2 select-none">
                    <li>
                        Перегляд списку бірж
                        <ul class="list-circle pl-8">
                            <li> 
                                <span class="font-medium">Основний виконавець:</span> 
                                Користувач
                            </li>

                            <li> 
                                <span class="font-medium">Зацікавлені особи та їх вимоги:</span> 
                                Користувач. Може переглянути список бірж
                            </li>

                            <li> 
                                <span class="font-medium">Передумови:</span>
                                Користувач запустив програму
                            </li>

                            <li> 
                                <span class="font-medium">Результат:</span>
                                На екрані користувача з‘явилася сторінка програми зі списком бірж 
                            </li>

                            <li> 
                                <span class="font-medium">Основний успішний сценарій:</span>
                                Користувач переглядає список бірж
                            </li>
                        </ul>
                    </li>

                    <li class="pt-2">
                        Вибір біржи
                        <ul class="list-circle pl-8">
                            <li> 
                                <span class="font-medium">Основний виконавець:</span> 
                                Користувач
                            </li>

                            <li> 
                                <span class="font-medium">Зацікавлені особи та їх вимоги:</span> 
                                Користувач. Може обрати біржу
                            </li>

                            <li> 
                                <span class="font-medium">Передумови:</span>
                                Користувач відкрив сторінку зі списком бірж
                            </li>

                            <li> 
                                <span class="font-medium">Результат:</span>
                                На екрані користувача зі списком бірж червоним кольором виділено обрану біржу 
                            </li>

                            <li> 
                                <span class="font-medium">Основний успішний сценарій:</span>
                                Користувач обрав біржу
                            </li>
                        </ul>
                    </li>

                    <li class="pt-2">
                        Перегляд спику компаній
                        <ul class="list-circle pl-8">
                            <li> 
                                <span class="font-medium">Основний виконавець:</span> 
                                Користувач
                            </li>

                            <li> 
                                <span class="font-medium">Зацікавлені особи та їх вимоги:</span> 
                                Користувач. Може переглянути список бірж
                            </li>

                            <li> 
                                <span class="font-medium">Передумови:</span>
                                Користувач запустив програму
                            </li>

                            <li> 
                                <span class="font-medium">Результат:</span>
                                На екрані користувача з'явилася сторінка зі списком компаній
                            </li>

                            <li> 
                                <span class="font-medium">Основний успішний сценарій:</span>
                                Користувач переглядає список компаній
                            </li>
                        </ul>
                    </li>

                    <li class="pt-2">
                        Перегляд торгів
                        <ul class="list-circle pl-8">
                            <li> 
                                <span class="font-medium">Основний виконавець:</span> 
                                Користувач
                            </li>

                            <li> 
                                <span class="font-medium">Зацікавлені особи та їх вимоги:</span> 
                                Користувач. Може переглядати торги обраної біржі
                            </li>

                            <li> 
                                <span class="font-medium">Передумови:</span>
                                Користувач обрав біржу
                            </li>

                            <li> 
                                <span class="font-medium">Результат:</span>
                                На екрані користувача з'явилася сторінка з торгами
                            </li>

                            <li> 
                                <span class="font-medium">Основний успішний сценарій:</span>
                                Користувач переглядає торги на біржі
                            </li>
                        </ul>
                    </li>

                    <li class="pt-2">
                        Придбання акцій
                        <ul class="list-circle pl-8">
                            <li> 
                                <span class="font-medium">Основний виконавець:</span> 
                                Користувач
                            </li>

                            <li> 
                                <span class="font-medium">Зацікавлені особи та їх вимоги:</span> 
                                Користувач. Може розмістити заявку на придбання акцій
                            </li>

                            <li> 
                                <span class="font-medium">Передумови:</span>
                                Користувач обрав біржу та відкрив сторінку з торгами
                            </li>

                            <li> 
                                <span class="font-medium">Результат:</span>
                                Користувач надіслав біржі заявку на придбання акцій
                            </li>

                            <li> 
                                <span class="font-medium">Основний успішний сценарій:</span>
                                <br>1. З'являється віконце для придбання акцій
                                <br>2. Користувач обирає компанію, кількість акцій та ціну за акцію
                                <br>3. Користувач натискає кнопку придбати
                                <br>4. Біржа приймає заявку на придбання та оновлює список торгів
                            </li>

                            <li> 
                                <span class="font-medium">Розширення:</span>
                                <br>1. З'являється віконце для придбання акцій
                                <br>2. Користувач обирає компанію, кількість акцій та ціну за акцію
                                <br>3. Користувачу не вистачає коштів на придбання
                                <br>4. Користувач натискає кнопку для закриття віконця
                            </li>
                        </ul>
                    </li>

                    <li class="pt-2">
                        Продаж акцій
                        <ul class="list-circle pl-8">
                            <li> 
                                <span class="font-medium">Основний виконавець:</span> 
                                Користувач
                            </li>

                            <li> 
                                <span class="font-medium">Зацікавлені особи та їх вимоги:</span> 
                                Користувач. Може розмістити заявку на продаж акцій
                            </li>

                            <li> 
                                <span class="font-medium">Передумови:</span>
                                Користувач обрав біржу та відкрив сторінку з торгами
                            </li>

                            <li> 
                                <span class="font-medium">Результат:</span>
                                Користувач надіслав біржі заявку на продаж акцій
                            </li>

                            <li> 
                                <span class="font-medium">Основний успішний сценарій:</span>
                                <br>1. З'являється віконце для продажу акцій
                                <br>2. Користувач обирає компанію, кількість акцій та ціну за акцію
                                <br>3. Користувач натискає кнопку продати
                                <br>4. Біржа приймає заявку на продаж та оновлює список торгів
                            </li>

                            <li> 
                                <span class="font-medium">Розширення:</span>
                                <br>1. У користувача немає акцій
                                <br>2. Віконце не відкривається
                            </li>
                        </ul>
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