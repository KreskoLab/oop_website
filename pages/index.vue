<template>
  <div class="flex justify-center items-center md:pt-12 text-dark-900">

    <div class="w-full md:w-3/5 bg-amber-200 md:border-2 border-dark-600 md:rounded">

      <div class="p-5">

          <h1 class="text-3xl text-center font-medium select-none">Звіт з виконання курсової роботи</h1>
          <h1 class="text-3xl text-center font-medium select-none pt-1">на тему: Іммітація процесів функціонування біржи</h1>


          <h2 class="text-right font-medium text-2xl mt-6">виконав студент групи ІСТ-22с</h2>
          <h2 class="text-right font-medium text-2xl mb-2">Орлов Андрій</h2>

          <div class="flex flex-col py-8">

            <Vstup />

            <UML />

            <ClassUML />

            <ActionUML />

            <StructUML />

            <Examples />

            <Literatura />

            <Github />

          </div>

      </div>

    </div>


  </div>
</template>

<script>
export default {

}
</script>
