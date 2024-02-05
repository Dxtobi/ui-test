<script>
// @ts-nocheck

	



	/** @type {HTMLElement} */
	let more_options_menu_button
	/** @type {HTMLElement} */
	let more_back_drop



	const toggle_more_option_button=()=>{
		more_options_menu_button.classList.toggle('show');
		more_back_drop.classList.toggle('show')
	}


	
</script>

 <div class="flex justify-between items-center px-4">
		<div class="flex gap-2 items-center">
		  <a href="/user/id" class="rounded-full  h-[60px] w-[60px] grid place-content-center  border-custom  border-2">
			<img src="/users/me8.jfif" alt="user" class="rounded-full  h-[50px] w-[50px] object-cover"/>
		  </a>
		  <div class="flex flex-col">
			<h2 class="font-bold">joseph adagbo</h2>
			<small class="font-extralight text-gray-500">32min ago</small>
		  </div>
		</div>
		<button class={`text-3xl`} on:click={toggle_more_option_button} >
			<iconify-icon icon={"ri:more-line"}></iconify-icon>
		</button>
		<button  on:click={toggle_more_option_button}  bind:this={more_back_drop} class="model-back-drop" />
		<model class="post-model" bind:this={more_options_menu_button}>
			<button>Add to bookmark</button>
			<button>Block this user</button>
			<button>Other commands 1</button>
		</model>
	  </div>

