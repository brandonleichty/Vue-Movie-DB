<template>
  <div>
    {{ movie.title }}
  </div>
</template>

<script>
export default {
	name: 'MoviesList',
  data() {
    return {
      movie: {}
    }
  },
  created: function() {
    this.fetchData();
  },
	methods: {
		fetchData: async function() {
			try {
				const res = await fetch(
					'https://api.themoviedb.org/3/movie/550?api_key=d951026be8c262501cf4a37f22f82184'
				);
				const movie = await res.json();
				this.movie = movie;
			} catch (e) {
				console.log(e);
			}
		}
	}
};
</script>

<style>
</style>
