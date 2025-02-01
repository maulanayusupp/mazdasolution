<template>
<div>
    <main>
        <!-- Rules -->
        <div class="overflow-hidden bg-white py-24 sm:py-32">
            <div class="mx-auto max-w-7xl px-6 lg:px-8">
                <div class="max-w-sm mx-auto text-center">
                    <img src="/assets/images/logos/logo.jpeg" alt="Product screenshot" class="w-full max-w-none rounded-xl shadow-xl ring-1 ring-gray-400/10 md:-ml-4 lg:-ml-0" width="2432" height="1442" />
                </div>
                
                <div class="mt-10">
                    <div class="w-full">
                        <p class="mt-10 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
                            Peraturan Keanggotaan
                        </p>
                        <dl class="mt-10 text-base leading-7 text-gray-600 lg:max-w-none grid grid-cols-1 md:grid-cols-2">
                            <div v-for="mission in missions" :key="mission.name" class="relative pl-9 mb-6">
                                <dt class="inline font-semibold text-gray-900">
                                    <component :is="mission.icon" class="absolute left-1 top-1 h-5 w-5 text-yellow-600" aria-hidden="true" />
                                    {{ mission.name }}
                                </dt>
                                {{ ' ' }}
                                <dd class="inline">{{ mission.description }}</dd>
                            </div>
                        </dl>
                    </div>
                </div>
            </div>
        </div>

    </main>
</div>
</template>

<script setup>
import { ref } from 'vue'

import { StarIcon } from '@heroicons/vue/20/solid'
import HeroSection from '~/components/home/HeroSection.vue';

const missions = [
    {
        name: 'No SARA (Suku, Agama, Ras, Antargolongan)',
        description: 'Semua anggota dilarang membahas atau menyentuh isu-isu sensitif terkait perbedaan suku, agama, ras, atau golongan. Mari jaga kerukunan dan saling menghormati.',
        icon: StarIcon,
    },
    {
        name: 'No Politics',
        description: 'Dilarang keras untuk membahas atau mengemukakan pandangan politik. Komunitas ini ada untuk berbagi kebahagiaan dan hobi, bukan untuk berdebat soal politik.',
        icon: StarIcon,
    },
    {
        name: 'No Pornography',
        description: 'Semua bentuk konten pornografi atau yang berbau tidak senonoh dilarang di komunitas ini. Kita saling menjaga kenyamanan satu sama lain.',
        icon: StarIcon,
    },
    {
        name: 'No Sindir-Sindiran',
        description: 'Hindari sindiran atau kata-kata yang bisa menyinggung perasaan orang lain. Komunitas ini adalah tempat untuk bersenang-senang, bukan untuk saling menjatuhkan.',
        icon: StarIcon,
    },
    {
        name: 'No Baper (Bawa Perasaan)',
        description: 'Jangan terlalu membawa perasaan. Kalau ada yang kurang cocok, diskusikan dengan kepala dingin. Jangan biarkan perbedaan pendapat merusak hubungan kita.',
        icon: StarIcon,
    },
    {
        name: 'Bermanfaat untuk Semua',
        description: 'Fokus kita adalah membuat komunitas ini bermanfaat bagi semua anggota. Ayo berbagi pengetahuan, pengalaman, dan informasi yang berguna.',
        icon: StarIcon,
    },
    {
        name: 'Silaturahmi dan Kebersamaan',
        description: 'Kita menjaga silaturahmi dan saling mendukung antar sesama anggota. Jangan ragu untuk berbagi, bertanya, atau membantu.',
        icon: StarIcon,
    },
    {
        name: 'Turing dan Kegiatan Bersama',
        description: 'Kami mendukung kegiatan turing dan acara komunitas lainnya yang positif. Ayo berpartisipasi untuk mempererat tali persaudaraan.',
        icon: StarIcon,
    },
]
</script>