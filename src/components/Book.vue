<script>
import Pay from './Pay.vue';
export default {
    components: {
        Pay,
    },
    props: {
        index: {
            type: Array,
        }
    },
    data() {
        return {
            showModal: false
        }
    },
    methods: {
        openModal() {
            this.showModal = true;
        },
        closeModal() {
            this.showModal = false;
        },
        bookingSuccess() {
            this.showModal = false;
            this.$emit('home');
        }
    }
}
</script>

<template>
    <div class="w-full min-h-screen fixed overflow-hidden">
        <div class="absolute inset-0 bg-cover bg-center scale-110"
            style="background-image: url('https://images.unsplash.com/photo-1552858725-a19e7fcd3ac4?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8cm9vbSUyMGhvdGVsJTIwZGFya3xlbnwwfHwwfHx8MA%3D%3D'); filter: blur(8px);">
        </div>

        <div class="relative w-full min-h-screen mt-14 bg-black/40 px-4 md:px-8 lg:px-16 py-10">
            <h2 class="text-4xl font-bold text-center mb-10 text-green-400">Booking Page</h2>

            <div v-if="index" class="w-220 h-140 max-w-2xl mx-auto bg-gray-800 rounded-lg shadow-lg overflow-hidden ">
                <img :src="index.image" class="w-full h-80 object-cover" alt="" />
                <div class="p-6 text-white">
                    <h3 class="text-xl font-bold mb-2">{{ index.name }}</h3>
                    <p class="text-gray-300 text-sm mb-4">{{ index.content }}</p>
                    <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4">
                        <div class="flex flex-col">
                            <span class="text-lg font-bold">${{ index.price }} / Night</span>
                            <span class="text-yellow-400 text-2xl">★★★★★</span>
                        </div>
                        <div class="flex gap-3">
                            <button
                                class="px-6 py-2 bg-red-600 rounded hover:bg-emerald-700 transition w-full sm:w-auto cursor-pointer">
                                Cancel
                            </button>
                            <button @click="openModal"
                                class="px-6 py-2 bg-green-600 rounded hover:bg-emerald-700 transition w-full sm:w-auto cursor-pointer">
                                Book
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <Pay v-if="showModal" @close-modal="closeModal" @booking-success="bookingSuccess" />
        </div>
    </div>
</template>