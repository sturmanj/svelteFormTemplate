<script>
    import { createEventDispatcher } from 'svelte';
    import { page0 } from './stores'
 
    const dispatch = createEventDispatcher();
 
    function next() {
        dispatch('message', {
            text: 'next'
        });
    }
</script>
 
<h1>PAGE 0</h1>
<input bind:value={$page0} />
<button on:click={next}> next </button>

