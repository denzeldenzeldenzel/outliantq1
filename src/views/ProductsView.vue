<template>
    <section class="w-full mt-24 px-10 sm:px-14 lg:px-40 py-4 bg-white">
        <div class="flex h-full items-start justify-between mx-auto max-w-7xl">
            <div class="flex flex-col justify-between w-full xl:w-3/5 space-y-10">
                <div class="flex flex-row justify-between w-full">
                    <h1 class="text-black font-bold text-left text-7xl">Products</h1>
                    <input class="border-black border-2 rounded-lg w-80 px-3 h-14 self-end"
                        placeholder="Search for keywords..." v-model="searchTerm" type="text">
                </div>
                <div class="w-full">
                    <table class="table-fixed w-full text-center">
                        <thead class="accent-gray border-t-black border-x-black border">
                            <tr class="h-14">
                                <th class="w-1/3 border-x-black border border-t-black text-base font-bold text-black">Name
                                </th>
                                <th class="w-1/3 border-x-black border border-t-black text-base font-bold text-black">Price
                                </th>
                                <th class="w-1/3 text-base font-bold text-black">Action</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr v-bind:key="index" v-for="(product, index) in filteredProducts" class="h-14">
                                <td class="border-x-black border border-b-black text-base font-medium text-neutral-500">
                                    {{ product.name }}</td>
                                <td class="border-x-black border border-b-black text-base font-medium text-neutral-500">
                                    {{ product.price }}</td>
                                <td
                                    class="border-x-black border border-b-black text-base font-medium text-neutral-500 space-x-2">
                                    <button
                                        @click="editProduct(index)"
                                        class="bg-black font-normal text-xl rounded-lg px-4 py-2 text-white antialiased">
                                        Edit
                                    </button>
                                    <button
                                        @click="deleteProduct(index)"
                                        class="font-bold text-xl rounded-lg px-4 py-2 text-black bg-transparent border-solid border-black border-2 antialiased">
                                        Delete
                                    </button>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
            <div class="flex flex-col justify-between items-end w-full xl:w-2/5 space-y-10">
                <div class="invisible flex flex-row justify-end w-full">
                    <h1 class="text-black font-bold text-left text-7xl">Products</h1>
                </div>
                <div class="w-5/6 accent-gray py-10 flex flex-col justify-center items-center text-center space-y-6">
                    <h2 class="text-3xl font-bold">
                        Header Text
                    </h2>
                    <p class="text-neutral-500 text-xl">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit ut
                    </p>
                    <input class="bg-white rounded-lg w-80 px-3 h-14" placeholder="Name" v-model="name" type="text">
                    <input class="bg-white rounded-lg w-80 px-3 h-14" placeholder="Price" v-model="price" type="text">
                    <button 
                        v-if="!isEditing"
                        @click="createProduct"
                        class="bg-black font-normal text-xl rounded-lg px-4 py-2 text-white antialiased">
                        Create
                    </button>
                    <button 
                        v-if="isEditing"
                        @click="saveProduct"
                        class="bg-black font-normal text-xl rounded-lg px-4 py-2 text-white antialiased">
                        Save
                    </button>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "ProductsView",
    data() {
        return {
            products: [
                {
                    name: "Lorem Ipsum 1",
                    price: "Lorem Ipsum 1"
                },
                {
                    name: "Lorem Ipsum 2",
                    price: "Lorem Ipsum 2"
                },
                {
                    name: "Lorem Ipsum 3",
                    price: "Lorem Ipsum 3"
                },
            ],
            name: "",
            price: "",
            isEditing: false,
            currentProductIndex: 0,
            searchTerm:""
        }
    },
    methods: {
        createProduct() {
            this.products.push({
                name: this.name,
                price: this.price
            });
            this.name = "";
            this.price = "";
            console.log(this.searchTerm)
            console.log(this.filteredProducts)
        },
        editProduct(index) {
            this.isEditing = true;
            this.currentProductIndex = index;
            this.name = this.products[this.currentProductIndex].name;
            this.price = this.products[this.currentProductIndex].price;
        },
        saveProduct(){
            this.products[this.currentProductIndex].name = this.name;
            this.products[this.currentProductIndex].price = this.price;
            this.name = "";
            this.price = "";
            this.isEditing = false;
        },
        deleteProduct(index) {
            this.products.splice(index, 1);
        },
    },
    computed: {
        filteredProducts() {
            return this.products.filter((x) => {
                return x.name.toLowerCase().includes(this.searchTerm.toLowerCase());
            });
        }
    }
}

</script>

<style scoped>
.accent-gray {
    background-color: #ececec;
}
</style>