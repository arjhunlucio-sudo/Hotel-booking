<script>
export default {
    data() {
        return {
        }
    },
    methods: {
        close() {
            this.$emit('close-modal');
        },
        submitBooking() {
            alert("Book Successfully!");
            this.$emit('booking-success');
        }
    }
}
</script>

<template>
    <div class="fixed top-0 inset-0 bg-black bg-opacity-80 flex items-center justify-center mt-20 z-50">
        <div class="bg-gray-600 p-4 rounded-lg shadow-2xl w-full max-w-md border border-gray-700">
            <h3 class="text-5xl font-bold text-black mb-2 text-center"><span class="text-5xl text-yellow-400">A</span>HOTEL</h3>
              <div class="flex">
                  <h3 class="text-2xl font-bold text-white mb-2 text-center">Booking Details</h3>
                </div>
            <div class="">
                <p class="block text-gray-300 mb-1">Check-in Date</p>
                <input type="number" class="w-full p-2 mb-3 rounded bg-gray-700 text-white border border-gray-600">

                <p class="block text-gray-300 mb-1">Check-in Time</p>
                <input  class="w-full p-2 rounded bg-gray-700 text-white border border-gray-600">
            </div>

            <div class="mb-6">
                <p class="block text-gray-300 mb-1">Check-out Date</p>
                <input type="number" class="w-full p-2 mb-3 rounded bg-gray-700 text-white border border-gray-600">

                <p class="block text-gray-300 mb-1">Check-out Time</p>
                <input  class="w-full p-2 rounded bg-gray-700 text-white border border-gray-600">
                <p class="block text-gray-300 mt-2">Payment</p>
                <input type="number" class="w-full p-2 rounded bg-gray-700 text-white border border-gray-600">

            </div>


            <div class="flex gap-3">
                <button @click="close"
                    class="w-1/2 py-2 bg-red-600 rounded text-white  cursor-pointer hover:bg-gray-500">
                    Cancel
                </button>
                <button @click="submitBooking"
                    class="w-1/2 py-2 bg-green-500 rounded cursor-pointer text-white hover:bg-emerald-700">
                    Confirm Booking
                </button>
            </div>

        </div>
    </div>
</template>