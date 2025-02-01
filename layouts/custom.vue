<template>
	<Html>
			<!-- Head -->
			<Head>
				<Title>Mazda Solution (MS) - Komunitas Pengguna Mazda Terbaik</Title>
				<Meta name="description" :content="`Bergabunglah dengan Mazda Solution (MS), komunitas penggemar dan pengguna Mazda yang penuh semangat. Dapatkan pengalaman berkendara yang seru, berbagi tips, dan ikuti kegiatan menarik bersama para pecinta Mazda lainnya.`" />
				<!-- <Link rel="preload" href="/test.txt" as="script" /> -->
				<!-- <Style type="text/css" :children="styleString" /> -->
			</Head>

			<!-- Header -->
			<nav-header />

			<!-- Content -->
			<slot />

			<!-- Footer -->
			<the-footer />
	</Html>
</template>

<script>
definePageMeta({
  layout: "custom",
});

import NavHeader from '@/layouts/partials/NavHeader.vue'
import TheFooter from '@/layouts/partials/TheFooter.vue'

export default {
	components: {
		NavHeader,
		TheFooter,
	},
	setup() {
		return {
		}
	},
}
</script>

