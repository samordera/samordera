<script lang="ts">
	import '../app.postcss';
	import { AppBar } from '@skeletonlabs/skeleton';
	import logo from '$lib/img/core/logo_no-bg.png'
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
</script>


<AppBar
background="bg-black text-yellow-200">
	<svelte:fragment slot="lead">
		<img src="{logo}"
		alt="logo"
		class="w-10">
	</svelte:fragment>
	<svelte:fragment slot="trail">
		<a href="">X</a>
		<a href="">GitHub</a>
		<a href="">LinkedIn</a>
	</svelte:fragment>
	<svelte:fragment slot="headline">
		Sam
	</svelte:fragment>
</AppBar>
<slot />
