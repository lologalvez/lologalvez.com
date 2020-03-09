<template>
	<div class="author">

		<g-image alt="Author image" class="author__image" src="~/assets/images/author.jpg" width="180" height="180" blur="5" />

		<h1 v-if="showTitle" class="author__site-title">
			{{ $static.metadata.siteName }}
		</h1>

		<p class="author__intro">
			Software Developer
			<br/>
			aspiring crafter | learning maniac | long-time lurker
		</p>
		<p class="author__intro">
		</p>

		<p class="author__links">
			<a href="//twitter.com/lologalvez"><font-awesome :icon="['fab', 'twitter']" size="lg"/></a>
			<a href="//github.com/lologalvez"><font-awesome :icon="['fab', 'github']" size="lg"/></a>
			<a href="//linkedin.com/in/manuel-galvez/"><font-awesome :icon="['fab', 'linkedin-in']" size="lg"/></a>
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
	siteDescription
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author {
	font-family: 'Montserrat', sans-serif;
	margin: 0 auto;
	max-width: 550px;
	text-align: center;
	padding: calc(var(--space) / 2) 0;

	&__image {
		border-radius: 100%;
		width: 90px;
		height: 90px;
		margin-bottom: 1em;
		border: 3px solid teal;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		font-size: 1.5em;
		color: teal;
	}

	&__links {
		margin-top: -.5em;
		a {
			color: teal;
			margin: 0 .7em;
		}
	}


}
</style>
