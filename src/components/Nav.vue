<template>
        <div v-if="mobileNav" class=" bg-gray-500 absolute top-0 left-0 w-full h-screen z-40 opacity-90">
            <ul class="flex flex-col justify-center items-center h-full space-y-4">
               <li class="text-5xl"><a href="/">Home</a></li> 
               <li class="text-5xl"><a href="">About</a></li> 
               <li class="text-5xl"><a href="">Services</a></li> 
               <li class="text-5xl"><a href="/products">Products</a></li> 
            </ul>
            <div @click="mobileNav = !mobileNav" class="absolute top-0 right-0 text-6xl pr-10 pt-10">X</div>
        </div>
        <header class="sticky top-0 z-30 w-full px-10 sm:px-14 lg:px-40 py-4 bg-white ">
            <div class="flex items-center justify-between mx-auto max-w-7xl">
                <a href="#">
                    <span class="text-3xl text-gray-900 font-bold">Logo <span class="text-xs">©</span></span>
                </a>
                <div class="flex items-center space-x-1">
                    <ul class="hidden space-x-2 md:inline-flex">
                        <li><a href="/" :class="{
                            'underline': isHome }"
                                class="px-4 py-2 font-semibold text-gray-600 rounded">Home</a></li>
                        <li><a href="#" class="px-4 py-2 font-semibold text-gray-600 rounded">About</a></li>
                        <li><a href="#" class="px-4 py-2 font-semibold text-gray-600 rounded">Services</a></li>
                        <li><a href="/products" :class="{
                            'underline': isProducts }"
                            class="px-4 py-2 font-semibold text-gray-600 rounded">Products</a></li>

                    </ul>
                    <div class="inline-flex md:hidden">
                        <button @click="mobileNav = !mobileNav" class="flex-none px-2 ">
                            <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24"
                                stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 8h16M4 16h16" />
                            </svg>
                            <span class="sr-only">Open Menu</span>
                        </button>
                    </div>
                </div>
                <div class="hidden md:block">
                    <button class="bg-black font-normal text-xl rounded-lg px-8 py-4 text-white antialiased">
                        Call to Action
                    </button>
                </div>
            </div>
        </header>
</template>
<script>
export default {
    name: "Nav",
    data() {
        return {
            mobileNav: false
        }
    },
    computed: {
        isHome() {
            return this.$route.name == "home";
        },
        isProducts() {
            return this.$route.name == "products";
        }
    }
}
</script>