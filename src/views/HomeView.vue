<template>
  <section class="w-full mt-44 px-10 sm:px-14 lg:px-40 py-4 bg-white">
    <div class="flex h-full items-center justify-between mx-auto max-w-7xl">
            <div class="w-full xl:w-2/5 items-center justify-center space-y-10 h-2/3">
              <h1 class="text-black font-bold text-left text-7xl">
                Lorem ipsum dolor sit amet consectur
              </h1>
              <h2 class="text-neutral-500 text-2xl">
                Lorem ipsum dolor sit amet consectur adipiscing elit ut aliquam, purus sit amet luctus venatis, lectus
              </h2>
              <div class="flex flex-row space-x-2">
                <button class="bg-black font-normal text-xl rounded-lg px-8 py-4 text-white antialiased">
                    Call to Action
                </button>
                <button class="font-bold text-xl rounded-lg px-8 py-4 text-black bg-transparent border-solid border-black border-2 antialiased">
                    See Workspace
                </button>
              </div>
            </div>
            <div class="hidden xl:block relative items-center w-1/2 h-2/3">
              <div class="hidden 2xl:block square"></div>
              <div class="hidden xl:block 2xl:hidden squareSmall"></div>
              <div class="hidden 2xl:block absolute -top-24 right-0 square2"></div>
            </div>
        </div>
  </section>
  <section class="w-full section2 mt-44 px-10 sm:px-14 lg:px-40 py-4 bg-neutral-200  xl:bg-white ">
    <div class="flex h-full items-center space-x-10 xl:space-x-0 xl:items-start justify-between mx-auto max-w-7xl">
            <div class="w-full xl:w-1/5 items-center justify-center space-y-5 h-1/3">
              <h3 class="text-black font-bold text-left text-2xl">
                Header Text
              </h3>
              <p class="text-neutral-500 text-xl">
                Lorem ipsum dolor sit amet,
                consectur adipiscing elit ut
                aliquam, purus sit amet luctus
                venatis, lectus magna fringila urna,
                porttitor rhoncus dolor purus non
                enim dolor.
              </p>
            </div>
            <div class="hidden 2xl:block w-2/5 h-full">
              <div class="square"></div>
            </div>
            <div class="hidden xl:block 2xl:hidden w-2/5 h-full">
              <div class="squareSmall"></div>
            </div>
            <div class="w-full xl:w-1/5 items-center justify-center space-y-5 h-1/3 xl:self-end">
              <h3 class="text-black font-bold text-left text-2xl">
                Header Text
              </h3>
              <p class="text-neutral-500 text-xl">
                Lorem ipsum dolor sit amet,
                consectur adipiscing elit ut
                aliquam, purus sit amet luctus
                venatis, lectus magna fringila urna,
                porttitor rhoncus dolor purus non
                enim dolor.
              </p>
            </div>
        </div>
  </section>

</template>


<script>
export default {
  name: "HomeView"
}

</script>

<style>
.square2 {
  width: 300px;
  height: 300px;
  background-color: #9d9d9d;
}
.square {
  width:600px;
  height:600px;
  background-color: #c4c4c4;
}
.squareSmall {
  width:450px;
  height:450px;
  background-color: #c4c4c4;
}
.section2{
  height: 600px;
}
</style>