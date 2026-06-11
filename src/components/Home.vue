<script>
import Book from './Book.vue';

export default {
    components: {
        Book

    },
    data() {
        return {
            currentPage: 'home',
            selectedRoom: [],

            rooms: [
                {
                    id: 1,
                    image: 'https://plus.unsplash.com/premium_photo-1661962340349-6ea59fff7e7b?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mjl8fHJvb20lMjBob3RlbHxlbnwwfHwwfHx8MA%3D%3D',
                    name: ' Entry-level, compact, basic amenities, 1–2 guests, standard bed, simple view',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '700.00',
                    descrip: 'Twin',
                },
                {
                    id: 2,
                    image: 'https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?w=500&auto=format&fit=crop&q=60',
                    name: 'Wider doors, grab bars, roll-in shower, wheelchair-friendly.',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '600.00',
                    descrip: 'Accessible Room'
                },
                {
                    id: 3,
                    image: 'https://images.unsplash.com/photo-1568495248636-6432b97bd949?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTV8fGhvdGVsJTIwcm9vbXxlbnwwfHwwfHx8MA%3D%3D',
                    name: ' Large room with separate sitting/lounge area, no full wall division.',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '200.00',
                    descrip: 'Junior Suite'
                },
                {
                    id: 4,
                    image: 'https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?w=500&auto=format&fit=crop&q=60',
                    name: 'Optimize your performance with our Physiotherapists',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '900.00',
                    descrip: 'Executive Room'
                },
                {
                    id: 5,
                    image: 'https://media.istockphoto.com/id/2149664000/photo/hotel-room-with-a-view.webp?a=1&b=1&s=612x612&w=0&k=20&c=QjvYTVyVvejwt2pQDRsBnrEaYtjGHtdOljwgIZkqShc=',
                    name: 'Extra space, 2–3 beds, often separate sleeping areas, for families.',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '500.00',
                    descrip: 'Family'
                },
                {
                    id: 6,
                    image: 'https://media.istockphoto.com/id/2233411830/photo/sunlit-bedroom-with-a-comfortable-double-bed-wooden-flooring-and-fresh-linens.webp?a=1&b=1&s=612x612&w=0&k=20&c=nv1JHENagSOfG6KGl5S8H-FcAoeBsHptZ3222khw8Zk=',
                    name: 'Entry-level, compact, basic amenities, 1–2 guests, standard bed, simple view.',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '300.00',
                    descrip: 'Standard '
                },
                {
                    id: 7,
                    image: 'https://images.unsplash.com/photo-1590490360182-c33d57733427?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fGhvdGVsJTIwcm9vbXxlbnwwfHwwfHx8MA%3D%3D',
                    name: 'Spacious, premium bedding, nicer decor, good view, extra amenities.',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '400.00',
                    descrip: 'Deluxe'
                },
                {
                    id: 8,
                    image: 'https://media.istockphoto.com/id/1370825295/photo/modern-hotel-room-with-double-bed-night-tables-tv-set-and-cityscape-from-the-window.webp?a=1&b=1&s=612x612&w=0&k=20&c=XJeW83B-wUlivdf2ciNAlRAV07aRr03xT-OfpQvwktg=',
                    name: 'Basic, affordable room with 1 bed or 2 twin beds, en-suite bathroom, TV, and basic amenities; good for short stays or solo travelers.',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '200.00',
                    descrip: 'Standard / Classic'
                },
                {
                    id: 9,
                    image: 'https://images.unsplash.com/photo-1722763529109-2bcb289a47c3?q=80&w=1315&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
                    name: 'Near pool/garden, private patio or direct pool access, casual resort-style design',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '200.00',
                    descrip: 'Cabana '
                },
                {
                    id: 10,
                    image: 'https://images.unsplash.com/flagged/photo-1556438758-8d49568ce18e?q=80&w=1174&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
                    name: 'Larger than standard (28–35 m²), better view, upgraded furniture, extra amenities like coffee maker or premium toiletries.',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '200.00',
                    descrip: 'Superior'
                },
                {
                    id: 10,
                    image: 'https://images.unsplash.com/photo-1631049421450-348ccd7f8949?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
                    name: 'Larger than standard (28–35 m²), better view, upgraded furniture, extra amenities like coffee maker or premium toiletries.',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '200.00',
                    descrip: 'Superior'
                },
                {
                    id: 10,
                    image: 'https://images.unsplash.com/flagged/photo-1556438758-8d49568ce18e?q=80&w=1174&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
                    name: 'Larger than standard (28–35 m²), better view, upgraded furniture, extra amenities like coffee maker or premium toiletries.',
                    content: "Smart comfort at a great price—our standard rooms give you everything you need for a pleasant, affordable stay.",
                    price: '200.00',
                    descrip: 'Superior'
                },
            ]
        }
    },
    methods: {
        selectRoom(index) {
            this.selectedRoom = index;
            this.currentPage = 'booking';
        }
    }
}
</script>

<template>
    <div>
        <Book v-if="currentPage === 'booking'" :index="selectedRoom" />
        <div v-if="currentPage === 'home'">
            <section
                class="w-full flex items-center justify-center min-h-screen overflow-hidden bg-gradient-to-b from-[#10111D] to-green-300">
                <div class="absolute inset-0 bg-black bg-opacity-50"></div>
                <div class="relative z-10 container mx-auto px-4 text-center text-white">
                    <h1 class="mb-6 text-4xl font-bold tracking-tight sm:text-5xl md:text-6xl lg:text-7xl"
                        style="line-height: 1.2">
                        "Unwind <span class="relative whitespace-nowrap text-green-300 dark:text-green-400">
                            <svg aria-hidden="true" viewBox="0 0 418 42"
                                class="absolute top-2/3 left-0 h-[0.58em] w-full fill-pink-400/70 dark:fill-pink-300/60"
                                preserveAspectRatio="none">
                                <path
                                    d="M203.371.916c-26.013-2.078-76.686 1.963-124.73 9.946L67.3 12.749C35.421 18.062 18.2 21.766 6.004 25.934 1.244 27.561.828 27.778.874 28.61c.07 1.214.828 1.121 9.595-1.176 9.072-2.377 17.15-3.92 39.246-7.496C123.565 7.986 157.869 4.492 195.942 5.046c7.461.108 19.25 1.696 19.17 2.582-.107 1.183-7.874 4.31-25.75 10.366-21.992 7.45-35.43 12.534-36.701 13.884-2.173 2.308-.202 4.407 4.442 4.734 2.654.187 3.263.157 15.593-.780 35.401-2.686 57.944-3.488 88.365-3.143 46.327.526 75.721 2.23 130.788 7.584 19.787 1.924 20.814 1.98 24.557 1.332l.066-.011c1.201-.203 1.53-1.825.399-2.335-2.911-1.31-4.893-1.604-22.048-3.261-57.509-5.556-87.871-7.36-132.059-7.842-23.239-.254-33.617-.116-50.627.674-11.629.540-42.371 2.494-46.696 2.967-2.359.259 8.133-3.625 26.504-9.810 23.239-7.825 27.934-10.149 28.304-14.005 .417-4.348-3.529-6-16.878-7.066Z" />
                            </svg>
                            <span class="relative "> in comfort, stay in style — your perfect</span>
                        </span> getaway starts here at our hotel!"
                    </h1>
                    <p class="mx-auto  max-w-3xl text-2xl">
                        "Relax, recharge, and create wonderful memories at our welcoming hotel"
                    </p>
                </div>
            </section>

            <div class="w-full flex flex-col md:flex-row py-20 dark:bg-black">
                <div class="flex flex-col w-[90%] lg:w-4/5 2xl:w-3/5 mx-auto">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-5 w-full">
                        <div @click="selectRoom(index)" v-for="index in rooms" :key="index.id"
                            class="border hover:scale-105 duration-300 border-gray-100 cursor-pointer dark:border-gray-600 rounded-md mt-6">
                            <div class="relative">
                                <img :src="index.image" class="w-full max-h-80" alt="" />
                                <div class="absolute bg-emerald-600 px-3 py-1 top-3 right-3 text-white text-sm">Wifi —
                                    TV</div>
                            </div>
                            <div class="p-4">
                                <p class="text-xl text-gray-400"><span class="text-xl text-yellow-300">A</span>HOTEL
                                    ROOM</p>
                                <h3 class="text-xl font-bold text-gray-600"><span class="text-emerald-600">{{
                                    index.descrip }}</span>
                                    Room</h3>
                                <h4 class="text-gray-500">{{ index.name }}</h4>
                                <p class="text-sm text-gray-500 mt-2">{{ index.content }}</p>
                            </div>
                            <div
                                class="p-4 border-t border-gray-100 dark:border-gray-600 flex justify-between items-center">
                                <span class="dark:text-gray-400">${{ index.price }} / Night</span>
                                <span class="text-yellow-400 text-2xl">★★★★★</span>
                            </div>
                            <div class="flex justify-center mb-5 ">
                                <button
                                    class="text-black w-40 p-4 rounded-md bg-green-400 cursor-pointer font-bold border">View
                                    rates</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="bg-black bg-cover flex justify-center w-full" style="height: 100vh;">
            <iframe width="100%" height="100%"
                src="https://www.youtube.com/embed/7dKIrnQQ3eQ?si=Uo8wjZ_YBpNIt2Mg&amp;start=6"
                title="YouTube video player" frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        </div>
    </div>
</template>