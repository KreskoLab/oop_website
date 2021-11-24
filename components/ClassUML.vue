<template>
    <div class="border-t-2 py-4 border-dark-900">

        <div class="flex flex-row justify-between items-center">

            <h2 class="text-2xl font-medium select-none">UML-діаграма класів</h2>
            
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
                <img class="mx-auto" src="@/assets/3.png">
                <img class="mx-auto" src="@/assets/4.png">
                <p class="text-center text-xl pt-5">Діаграма класів</p>
            </div> 

            <div class="mt-6">

                <ul class="list-decimal text-xl pl-6 pt-2 select-none">

                    <li class="pt-2">
                        <span class="font-medium">Клас Stock (призначений для відображення даних про біржі)</span>

                        <p class="font-medium pt-2">Поля:</p>

                        <ul class="list-circle pl-8">
                            <li class="pt-2"> 
                                <span>string name:</span> 
                                атрибут для збереження назви біржі
                            </li>

                            <li class="pt-2"> 
                                <span>string code:</span> 
                                атрибут для збереження коду біржі
                            </li>

                            <li class="pt-2"> 
                                <span>string img:</span> 
                                атрибут для збереження шляху зображення біржі
                            </li>

                            <li class="pt-2"> 
                                <span>array companies:</span> 
                                атрибут для збереження спику компаній біржи
                            </li>

                            <li class="pt-2"> 
                                <span>array traders:</span> 
                                атрибут для збереження спику трейдерів біржи
                            </li>

                            <li class="pt-2"> 
                                <span>object requirements:</span> 
                                атрибут для збереження переліку вимог біржи
                            </li>

                            <li class="pt-2"> 
                                <span>object requirements:</span> 
                                атрибут для збереження переліку вимог біржи
                            </li>

                            <li class="pt-2"> 
                                <span>number fee:</span> 
                                атрибут для збереження комісії біржи
                            </li>

                            <li class="pt-2"> 
                                <span>array asks:</span> 
                                атрибут для збереження списку заяв на продаж акцій біржи
                            </li>

                            <li class="pt-2"> 
                                <span>array bids:</span> 
                                атрибут для збереження списку заяв на придбання акцій біржи
                            </li>

                        </ul>
                    </li>


                    <p class="font-medium">Конструктори:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>Stock(string name, code, img, array companies, traders, asks, bids, object requirements, number fee ):</span> 
                            конструктор з параметрами, у якому атрибутам присвоюється значеня параметрів
                        </li>
                    </ul>

                    <p class="font-medium">Методи:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>getName():</span> 
                            метод призначений для отримання назви біржі
                        </li>
                        <li class="pt-2"> 
                            <span>getCode():</span> 
                            метод призначений для отримання коду біржі
                        </li>
                        <li class="pt-2"> 
                            <span>getRequirements():</span> 
                            метод призначений для отримання вимог біржі до компаній
                        </li>
                        <li class="pt-2"> 
                            <span>getAsks():</span> 
                            метод призначений для отримання спику заяв на продаж акцій
                        </li>
                        <li class="pt-2"> 
                            <span>getBids():</span> 
                            метод призначений для отримання спику заяв на придбання акцій
                        </li>
                        <li class="pt-2"> 
                            <span>checkCompany(object company):</span> 
                            метод призначений для перевірки компанії на вимоги біржі
                        </li>
                        <li class="pt-2"> 
                            <span>acceptCompany(object company):</span> 
                            метод призначений для прийому компанії на біржу
                        </li>
                        <li class="pt-2"> 
                            <span>acceptTrader(object trader):</span> 
                            метод призначений для прийому трейдера на біржу
                        </li>
                        <li class="pt-2"> 
                            <span>newAsk(amount, price, share: number, company_name, user_name: string, is_player: boolean):</span> 
                            метод призначений для прийому заявки на продаж акцій
                        </li>
                        <li class="pt-2"> 
                            <span>newBid(amount, price, share: number, company_name, user_name: string, is_player: boolean):</span> 
                            метод призначений для прийому заявки на придбання акцій
                        </li>
                        <li class="pt-2"> 
                            <span>processing()</span> 
                            метод призначений для обробки заяв на придбання та продаж акцій біржою
                        </li>
                    </ul>



                    <li class="pt-2">
                        <span class="font-medium">Клас StocksFactory (призначений для створення екземплярів класу Stock)</span>

                        <p class="font-medium pt-2">Поля:</p>

                        <ul class="list-circle pl-8">
                            <li class="pt-2"> 
                                <span>string saved_stocks_path:</span> 
                                атрибут зі шляхом до файла з збереженними біржами
                            </li>

                            <li class="pt-2"> 
                                <span>array saved_stocks:</span> 
                                атрибут для завантажених списку збереженних бірж
                            </li>

                            <li class="pt-2"> 
                                <span>string stocks_file_path:</span> 
                                атрибут зі шляхом до файла з дефолтними біржами
                            </li>

                            <li class="pt-2"> 
                                <span>array stocks_file:</span> 
                                атрибут для збереження спику дефолтних бірж
                            </li>

                            <li class="pt-2"> 
                                <span>array stocks:</span> 
                                атрибут для збереження спику бірж
                            </li>

                        </ul>
                    </li>


                    <p class="font-medium">Конструктори:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>StocksFactory():</span> 
                            конструктор без параметрів, у якому усім полям буде присвоєно значення за замовченням
                        </li>
                    </ul>

                    <p class="font-medium">Методи:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>create():</span> 
                            метод призначений для завантаження списку бірж з файлу та створення екземпляру класа Stock для кожної біржи
                        </li>
                        <li class="pt-2"> 
                            <span>getStocks():</span> 
                            метод призначений для отримання списку екземплярів класу Stock
                        </li>
                        <li class="pt-2"> 
                            <span>getStocksCodes():</span> 
                            метод призначений для отримання списку кодів бірж
                        </li>
                        <li class="pt-2"> 
                            <span>processStocks():</span> 
                            метод призначений для обробки заяв усіх бірж
                        </li>
                        <li class="pt-2"> 
                            <span>save():</span> 
                            метод призначений для збереження даних бірж у файл
                        </li>
                    </ul>



                    <li class="pt-2">
                        <span class="font-medium">Клас Companies (призначений для відображення даних про компанії)</span>

                        <p class="font-medium pt-2">Поля:</p>

                        <ul class="list-circle pl-8">
                            <li class="pt-2"> 
                                <span>string name:</span> 
                                атрибут для збереження назви компанії
                            </li>

                            <li class="pt-2"> 
                                <span>string type:</span> 
                                атрибут для збереження спеціалізації компанії
                            </li>

                            <li class="pt-2"> 
                                <span>string stock:</span> 
                                атрибут для збереження коду біржі на якій проводила лістинг компанія
                            </li>

                            <li class="pt-2"> 
                                <span>number revenue:</span> 
                                атрибут для збереження доходу компанії
                            </li>

                            <li class="pt-2"> 
                                <span>number capitalization:</span> 
                                атрибут для збереження капіталізації компанії
                            </li>

                            <li class="pt-2"> 
                                <span>object shares:</span> 
                                атрибут для збереження інформації про акції компанії
                            </li>

                        </ul>
                    </li>


                    <p class="font-medium">Конструктори:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>Company(name, type, stock: string, revenue, capitalization: number, shares: object):</span> 
                            конструктор з параметрами, у якому атрибутам присвоюється значеня параметрів
                        </li>
                    </ul>

                    <p class="font-medium">Методи:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>ipo(): boolean</span> 
                            метод призначений для проведення компанієй IPO
                        </li>
                        <li class="pt-2"> 
                            <span>is_free_shares(): boolean</span> 
                            метод призначений для перевірки чи має компанія вільні акції
                        </li>
                        <li class="pt-2"> 
                            <span>sell():</span> 
                            метод призначений для продажу своїх акції компанієй
                        </li>
                        <li class="pt-2"> 
                            <span>getStock():</span> 
                            метод призначений для отримання екземпляра класу біржі на якій провела лістинг компанія
                        </li>
                    </ul>


                    


                    <li class="pt-2">
                        <span class="font-medium">Клас CompaniesFactory (призначений для створення екземплярів класу Company)</span>

                        <p class="font-medium pt-2">Поля:</p>

                        <ul class="list-circle pl-8">
                            <li class="pt-2"> 
                                <span>string saved_companies_path:</span> 
                                атрибут зі шляхом до файла з збереженними компаніями
                            </li>

                            <li class="pt-2"> 
                                <span>string companies_names_path:</span> 
                                атрибут зі шляхом до файла з назвами для компаній
                            </li>

                            <li class="pt-2"> 
                                <span>string companies_types_path:</span> 
                                атрибут зі шляхом до файла з спеціалізаціями компаній
                            </li>

                            <li class="pt-2"> 
                                <span>array companies_names:</span> 
                                атрибут для завантаження списку назв компаній
                            </li>

                            <li class="pt-2"> 
                                <span>array companies_types:</span> 
                                атрибут для завантаження списку спеціалізацій компаній
                            </li>

                            <li class="pt-2"> 
                                <span>boolean boot:</span> 
                                атрибут прапорець який повідомляє що програма загрузилась
                            </li>

                            <li class="pt-2"> 
                                <span>array saved_companies:</span> 
                                атрибут для завантаження списку збереженних компаній
                            </li>

                            <li class="pt-2"> 
                                <span>array companies:</span> 
                                атрибут для збереження списку компаній
                            </li>

                        </ul>
                    </li>


                    <p class="font-medium">Конструктори:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>CompaniesFactory():</span> 
                            конструктор без параметрів, у якому усім полям буде присвоєно значення за замовченням
                        </li>
                    </ul>

                    <p class="font-medium">Методи:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>load():</span> 
                            метод призначений для завантаження збереженного списку компаній та створення екземпляру класа Company для кожної компанії
                        </li>
                        <li class="pt-2"> 
                            <span>create():</span> 
                            метод призначений для створення екземпляру класа Company
                        </li>
                        <li class="pt-2"> 
                            <span>sendCompanies():</span> 
                            метод призначений для відправки повідомлення зі списком компаній
                        </li>
                        <li class="pt-2"> 
                            <span>getCompanies(): array</span> 
                            метод призначений для отримання списку компаній
                        </li>
                        <li class="pt-2"> 
                            <span>getNoStockCompanies(): array</span> 
                            метод призначений для отримання списку компаній які не здійснили IPO
                        </li>
                        <li class="pt-2"> 
                            <span>sellShares()</span> 
                            метод призначений для продажу своїх акцій компаніями
                        </li>
                        <li class="pt-2"> 
                            <span>save()</span> 
                            метод призначений для збереження списку компаній у файлі
                        </li>
                    </ul>





                    <li class="pt-2">
                        <span class="font-medium">Клас Time (призначений для відображення часу)</span>

                        <p class="font-medium pt-2">Поля:</p>

                        <ul class="list-circle pl-8">
                            <li class="pt-2"> 
                                <span>number speed:</span> 
                                атрибут для збереження швидкості часу
                            </li>

                            <li class="pt-2"> 
                                <span>number day:</span> 
                                атрибут для збереження номера дня
                            </li>

                            <li class="pt-2"> 
                                <span>number month:</span> 
                                атрибут для збереження номера місяця
                            </li>

                            <li class="pt-2"> 
                                <span>number year:</span> 
                                атрибут для збереження року
                            </li>

                            <li class="pt-2"> 
                                <span>number quarter:</span> 
                                атрибут для збереження номера кварталу
                            </li>

                            <li class="pt-2"> 
                                <span>number old_quarter:</span> 
                                атрибут для збереження номера минулого кварталу
                            </li>

                            <li class="pt-2"> 
                                <span>string config:</span> 
                                атрибут зі шляхом до файла збереження2
                            </li>

                        </ul>
                    </li>


                    <p class="font-medium">Конструктори:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>Time():</span> 
                            конструктор без параметрів, у якому усім полям буде присвоєно значення за замовченням
                        </li>
                    </ul>

                    <p class="font-medium">Методи:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>start()</span> 
                            метод призначений для завантаження значень полів з файлу та початку відліку часу
                        </li>
                        <li class="pt-2"> 
                            <span>getDate(): string</span> 
                            метод призначений для отримання дати
                        </li>
                        <li class="pt-2"> 
                            <span>getSpeed(): number</span> 
                            метод призначений для отримання швидкості часу
                        </li>
                        <li class="pt-2"> 
                            <span>getQuarter(): number</span> 
                            метод призначений для отримання квартала
                        </li>
                        <li class="pt-2"> 
                            <span>newQuarter()</span> 
                            метод призначений для відправки повідомлення про новий квартал
                        </li>
                        <li class="pt-2"> 
                            <span>newDay()</span> 
                            метод призначений для відправки повідомлення про новий день
                        </li>
                        <li class="pt-2"> 
                            <span>newDay()</span> 
                            метод призначений для збереження полів у файл збереження
                        </li>
                    </ul>




                    <li class="pt-2">
                        <span class="font-medium">Клас Trader (призначений для відображення даних про трейдерів)</span>

                        <p class="font-medium pt-2">Поля:</p>

                        <ul class="list-circle pl-8">
                            <li class="pt-2"> 
                                <span>string number:</span> 
                                атрибут для збереження ім'я трейдера
                            </li>

                            <li class="pt-2"> 
                                <span>number capital:</span> 
                                атрибут для збереження капіталу трейдера
                            </li>

                            <li class="pt-2"> 
                                <span>number revenue:</span> 
                                атрибут для збереження доходу трейдера
                            </li>

                            <li class="pt-2"> 
                                <span>array shares:</span> 
                                атрибут для збереження придбаних акцій трейдера
                            </li>

                            <li class="pt-2"> 
                                <span>string stock:</span> 
                                атрибут для збереження коду біржи трейдера
                            </li>

                            <li class="pt-2"> 
                                <span>number old_quarter:</span> 
                                атрибут для збереження номера минулого кварталу
                            </li>

                        </ul>
                    </li>


                    <p class="font-medium">Конструктори:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>Trader(name, stock: string, capital, revenue: number, shares: array):</span> 
                            конструктор з параметрами, у якому атрибутам присвоюється значення параметрів
                        </li>
                    </ul>

                    <p class="font-medium">Методи:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>enoughCapital(): boolean</span> 
                            метод призначений для перевірки чи достатньо у трейдера капіталу на придбання акцій
                        </li>
                        <li class="pt-2"> 
                            <span>buy():</span> 
                            метод призначений для придбання акцій
                        </li>
                        <li class="pt-2"> 
                            <span>sell():</span> 
                            метод призначений для продажу акцій
                        </li>
                    </ul>






                    <li class="pt-2">
                        <span class="font-medium">Клас TradersFactory (призначений для створення екземплярів класу Trader)</span>

                        <p class="font-medium pt-2">Поля:</p>

                        <ul class="list-circle pl-8">
                            <li class="pt-2"> 
                                <span>boolean boot:</span> 
                                атрибут прапорець який повідомляє що програма загрузилась
                            </li>

                            <li class="pt-2"> 
                                <span>string saved_traders_path:</span> 
                                атрибут зі шляхом до файла з збереженними трейдерами
                            </li>

                            <li class="pt-2"> 
                                <span>array saved_traders:</span> 
                                атрибут для завантаження списку збереженних трейдерів
                            </li>

                            <li class="pt-2"> 
                                <span>string traders_names_path:</span> 
                                атрибут зі шляхом до файла з іменами трейдерів
                            </li>

                            <li class="pt-2"> 
                                <span>array traders_names:</span> 
                                атрибут для завантаження списку імен трейдерів
                            </li>

                            <li class="pt-2"> 
                                <span>array traders:</span> 
                                атрибут для збереження списку трейдерів
                            </li>

                            <li class="pt-2"> 
                                <span>array stocks:</span> 
                                атрибут зі списком бірж
                            </li>

                        </ul>
                    </li>


                    <p class="font-medium">Конструктори:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>CompaniesFactory():</span> 
                            конструктор без параметрів, у якому усім полям буде присвоєно значення за замовченням
                        </li>
                    </ul>

                    <p class="font-medium">Методи:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>updateStocks():</span> 
                            метод призначений для оновлення списку бірж
                        </li>
                        <li class="pt-2"> 
                            <span>load():</span> 
                            метод призначений для завантаження списку збереженних трейдерів
                        </li>
                        <li class="pt-2"> 
                            <span>create(): array</span> 
                            метод призначений для створення нових екземплярів класу Trader
                        </li>
                        <li class="pt-2"> 
                            <span>tryBID()</span> 
                            метод призначений для придбання акцій трейдерами
                        </li>
                        <li class="pt-2"> 
                            <span>tryASK()</span> 
                            метод призначений для продажу своїх акцій трейдерами
                        </li>
                        <li class="pt-2"> 
                            <span>save()</span> 
                            метод призначений для збереження списку трейдерів у файлі збереження
                        </li>
                    </ul>






                    <li class="pt-2">
                        <span class="font-medium">Клас User розширює клас Trader (призначений для відображення даних користувача)</span>

                        <p class="font-medium pt-2">Поля:</p>

                        <ul class="list-circle pl-8">

                            <li class="pt-2"> 
                                <span>string saved_user_path:</span> 
                                атрибут зі шляхом до файла збереження
                            </li>

                            <li class="pt-2"> 
                                <span>object user:</span> 
                                атрибут для збереження даних користувача
                            </li>

                        </ul>
                    </li>


                    <p class="font-medium">Конструктори:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>User(name, stock: string, capital, revenue: number, shares: array):</span> 
                            конструктор з параметрами, у якому атрибутам присвоюється значення параметрів
                        </li>
                    </ul>

                    <p class="font-medium">Методи:</p>

                    <ul class="list-circle pl-8">
                        <li class="pt-2"> 
                            <span>load(): boolean</span> 
                            метод призначений для завантаження даних з файла збереження
                        </li>
                        <li class="pt-2"> 
                            <span>save():</span> 
                            метод призначений для збереження даних користувача у файл збереження
                        </li>
                        <li class="pt-2"> 
                            <span>getAll(): object</span> 
                            метод призначений для отримання усіх значень полів користувача
                        </li>
                        <li class="pt-2"> 
                            <span>getCapital(): number</span> 
                            метод призначений для отримання значення капіталу користувача
                        </li>
                        <li class="pt-2"> 
                            <span>getStock(): number</span> 
                            метод призначений для отримання коду біржі користувача
                        </li>
                        <li class="pt-2"> 
                            <span>updateStock(stock: string):</span> 
                            метод призначений для оновлення коду біржі користувача
                        </li>
                    </ul>





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