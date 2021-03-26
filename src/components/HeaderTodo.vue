<template>
	<div class="header__wrapper">
		<div class="header__body">
			<nav class="menu">
				<ul class="list">
					<li class="list__item" v-html="(link, index) in HeaderLinks" :key="index">
						{{ link }}
					</li>
				</ul>
			</nav>
		</div>
	</div>
</template>


<script>
	export default {
	    props: ['HeaderLinks'],
	}
</script>