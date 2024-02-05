<script>
	import BigNav from '$lib/components.g/BigNav.svelte';
  import Footer from '$lib/components.g/Footer.svelte';
import Header from '../lib/components.g/Header.svelte';
	import './styles.css';
	import 'iconify-icon'
</script>

<div class="app">
	<Header />


	<main class="md:w-[40%] m-auto my-20 md:my-4">
		<slot />
	</main>

	<BigNav/>
	<Footer/>
	
</div>

