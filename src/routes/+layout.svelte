<script>
	import logo from '$lib/assets/logo.svg';
	import stylesheet from '$lib/css/global-styles.css';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={logo} />
</svelte:head>

{@render children?.()}
