<template>
	<storyblok-wrapper url="home">
		<template #default="{ refreshKey }">
			<main :key="refreshKey" class="page-index layout-block">
				<home-intro />
				<home-portfolio />
			</main>
		</template>
	</storyblok-wrapper>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
.page-index {
}
</style>
