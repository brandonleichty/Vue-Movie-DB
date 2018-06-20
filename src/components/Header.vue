<template>
  <header>
    <h1><router-link to="/">
			<img src="../assets/logo.svg"/>
		</router-link></h1>
		<!-- <transition name="fade">
			<h1 v-if="show">Animated</h1>
		</transition>
		<button @click="show = !show">Show/Hide</button> -->
  </header>
</template>

<script>
export default {
	name: 'Header',
	props: {
		title: String
	},
	data() {
		return {
			show: false,
			name: 'Brandon'
		};
	},
};
</script>

<style scoped>
header {
	background-color: #111;
	padding: 20px;
	color: white;
}
h1 {
	margin: 0;
}

/* name-enter -> name-enter-to */
/* name-enter-active */

/* name-leave -> name-leave-to */
/* name-leave-active */
</style>
