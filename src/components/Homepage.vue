<template>
	<div class="hello">
		<h1>{{ title }}</h1>
		<h2>{{ taglines[Math.floor(Math.random() * taglines.length)].message }}</h2>
		<ul>
			<li v-for="link in links">
				<a v-bind:href="link.url"
					target="_blank"
				>
					{{ link.text }}
				</a>
			</li>
			<br>
		</ul>
	</div>
</template>

<script>
	export default {
		name: 'Welcome',
		data () {
			return {
				title: 'Kimball Bros',
				taglines: [
					{ message: 'dummy slogan 1' },
					{ message: 'dummy slogan 2' },
					{ message: 'dummy slogan 3' }
				],
				links: [
					{ 	
						text: 'Facebook',
						url: 'http://facebook.com' 
					},
					{ 	
						text: 'Twitter',
						url: 'http://twitter.com' 
					},
					{ 	
						text: 'Instagram',
						url: 'http://instagram.com' 
					}
				]
			}
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	h1, h2 {
		font-weight: normal;
	}
	ul {
		list-style-type: none;
		padding: 0;
	}
	li {
		display: inline-block;
		margin: 0 10px;
	}
	a {
		color: #123191;
	}
</style>
