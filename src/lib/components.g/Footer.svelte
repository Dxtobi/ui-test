
<script>
 // import { list } from 'postcss';
	import { onMount } from 'svelte';
    onMount(()=>{
       const list = document.querySelectorAll('.footer-link');

        const activeLink=()=> {
        
            list.forEach((elem)=>{
            elem.classList.remove('active__mobile');
            })
        }

        list.forEach((elem)=>{elem.addEventListener('click', (e)=>{
            activeLink()
            elem.classList.add('active__mobile');
            // @ts-ignore
            var position = elem.offsetLeft + elem.offsetWidth/2 ;
    
    // Set the indicator's transform property to move it to the clicked item
    // @ts-ignore
    document.querySelector('.indicator').style.transform = 'translateX(calc(' + position + 'px - 52px))';
            console.log(e)
        })})
    })
</script>

<div class="fixed bottom-0 left-0 w-screen md:hidden footer__ z-[10]">
  <div class="list">
    <a href="/home" class="footer-link active__mobile">
      <iconify-icon icon={"iconamoon:home-fill"} enableCache={true} class='icons-a'
      ></iconify-icon>
    </a>
    <a href="/about" class="footer-link ">
      <iconify-icon icon={"gala:chat"} enableCache={true} class='icons-a'></iconify-icon>
    </a>
    <a href="/about" class="footer-link">
      <iconify-icon icon={"pajamas:group"} enableCache={true} class='icons-a'></iconify-icon>
    </a>
    <a href="/about" class="footer-link">
      <iconify-icon icon={"iconamoon:profile-circle-thin"} enableCache={true} class='icons-a'
      ></iconify-icon>
    </a>
    
    <a href="/about" class="footer-link">
      <iconify-icon icon={"uiw:setting-o"} enableCache={true} class='icons-a'></iconify-icon>
    </a>
    <div class="indicator"></div>
  </div>
 
</div>

