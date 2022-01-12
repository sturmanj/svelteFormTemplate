<script>
	import Page1 from './Page0.svelte';
	import Page2 from './Page1.svelte';
	import { page0, page1 } from './stores'
   
	const pages = [Page1, Page2];
   
	let page = 0;
   
	  function handleMessage(event) {
		if (event.detail.text == 'next') {
		  page += 1;
		}
		if (event.detail.text == 'prev') {
		  page -= 1;
		}
		if (event.detail.text == 'sbmt') {
		  console.log({
			"page0": $page0,
			"page1": $page1
		  })
		  $page0 = ''
		  $page1 = ''
		  page = 0
		}
	  }
   
  </script>
   
  <svelte:component this={pages[page]} on:message={handleMessage}/>
  
  