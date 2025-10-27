<template>
	<storyblok-wrapper url="home">
		<template #default="{ story, refreshKey }">
			<main :key="refreshKey" class="page-index layout-block">
				<h1>{{ story.name }}</h1>
				<common-a-link href="/test">
					<p class="mono-large">Go To Test Page</p>
				</common-a-link>
				<p v-for="i in 100" :key="i">{{ i }}</p>
			</main>
		</template>
	</storyblok-wrapper>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
.page-index {
	padding: var(--spacer-64) 0;
}
</style>
