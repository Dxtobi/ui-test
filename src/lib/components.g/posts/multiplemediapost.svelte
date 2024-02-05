<script>
// @ts-nocheck

  import PostHeader from './PostHeader.svelte';

  
	/** @type {HTMLElement} */
	let fave
	/** @type {HTMLElement} */
	let more_options_menu_button
	/** @type {HTMLElement} */
	let more_back_drop

	const handle_like_comment =()=>{
		fave.classList.toggle('flip-animation')
	}

	const toggle_more_option_button=()=>{
		more_options_menu_button.classList.toggle('show');
		more_back_drop.classList.toggle('show')
	}


	const switch_images = ( /** @type {{ srcElement: string | Node; }} */ e)=>{
		// @ts-ignore
		document.getElementById('img-wrap').prepend(e.srcElement)
		// console.log(e.srcElement)
	}
</script>
 
 <section class="mt-8">
	  <!-- POST COMPONENT HEADER -->
	 <PostHeader/>
	   <!-- POST COMPONENT BODY -->
	   <div class="p-4">
		  <div class="relative w-full mt-1  rounded-xl " >
			<div id="img-wrap" class="img-wrap w-full">
			<div  role="button" aria-label="PANIC!" on:keydown={switch_images} tabindex="0" style="background-image: url(/users/me8.jfif); background-size: cover; " on:click={switch_images}   class="none-active-image parallax-container "></div>
			<div  role="button" aria-label="PANIC!" on:keydown={switch_images} tabindex="0" style="background-image: url(/users/me3.jfif); background-size: cover;" on:click={switch_images}  class="none-active-image"></div>
			<div  role="button" aria-label="PANIC!" on:keydown={switch_images} tabindex="0" style="background-image: url(/users/me5.jfif); background-size: cover;"  on:click={switch_images} class="none-active-image"></div>
			</div>
	  
			<div class="flex gap-2 items-center absolute bottom-4 left-4">
				<button id="favorite" bind:this={fave}  class="text-3xl shadow-2xl h-[50px] w-[50px] rounded-full backdrop-blur-[10px] bg-[#ffffff4a] flex justify-center items-center" on:click={handle_like_comment}>
					<iconify-icon icon="mdi:heart" enableCache></iconify-icon>
				  </button>
			  <span class="px-4 p-1 bg-[#ffffff4c] rounded-full backdrop-blur-2xl text-white shadow-2xl">405k</span>
			</div>
		  </div>
	   </div>
	  


	   <!-- FIRST COMMENT SECTION -->
	   <div class=" flex gap-2 px-4 items-center">
		 <div class="flex gap-0">
		  <img src="/users/me5.jfif" alt="ui" class="w-[30px] h-[30px] rounded-full  border-2" />
		  <img src="/users/me8.jfif" alt="ui" class="w-[30px] h-[30px] rounded-full ml-[-10px] border-2" />
		  <img src="/users/me7.jfif" alt="ui" class="w-[30px] h-[30px] rounded-full ml-[-10px] border-2" />
		 </div>

		 <p class="text-gray-600 whitespace-nowrap"> Liked by </p>
		 <p class="font-bold whitespace-nowrap overflow-clip ">programmer_dex</p>
		 <p class="text-gray-600 whitespace-nowrap"> and others </p>

	   </div>


	   <!-- POST CAPTION -->
	   <div class="px-4 font-semibold">
		<p class="line-clamp-2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure fugit voluptatibus cum dolores velit, reprehenderit iusto quae quo. Asperiores, blanditiis.</p>
	   </div>

	   <!-- OTHER COMMENTS -->
	   <div class="px-4">
		<p class="text-gray-600 whitespace-nowrap ">Over 30k comments </p>
		<div>
		  <p><strong>masked_man_boy </strong> nice illustration</p>
		</div>
	   </div>
	</section>

