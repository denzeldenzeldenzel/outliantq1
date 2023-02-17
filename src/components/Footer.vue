<template>
    <section class="custom-footer  mt-72 w-full px-10 sm:px-14 lg:px-40 ">
        <div class="flex flex-row h-full justify-start xl:space-x-20 mx-auto max-w-7xl">
            <div class="hidden 2xl:block relative footer-left">
                <div class="absolute square bottom-20 left-0"></div>
            </div>
            <div class="hidden xl:block 2xl:hidden relative footer-left-small">
                <div class="absolute squareSmall bottom-60 left-0"></div>
            </div>
            <div class="w-2/3 xl:w-1/3 xl:items-center xl:justify-center space-y-10 h-2/3 self-center">
                <h1 class="text-black font-bold text-left text-5xl 2xl:text-6xl">
                    Lorem ipsum dolor sit amet consectur
                </h1>
                <h2 class="text-neutral-500 text-2xl">
                    Lorem ipsum dolor sit amet consectur adipiscing elit ut aliquam, purus sit amet luctus venatis, lectus
                </h2>
                <button class="bg-black font-normal text-xl rounded-lg px-8 py-4 text-white antialiased">
                    Call to Action
                </button>
            </div>
        </div>

    </section>
</template>
<script>
export default {
    name: "Footer"
}
</script>
<style scoped>
.custom-footer {
    height: 600px;
    background-color: #ececec;
}
.footer-left {
    width:600px;
}

.footer-left-small{
    width:450px;
}
</style>