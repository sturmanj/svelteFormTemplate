<script>
    import { createEventDispatcher } from 'svelte';
    import { page1 } from './stores'
 
    const dispatch = createEventDispatcher();
 
    function prev() {
        dispatch('message', {
            text: 'prev'
        });
    }
    function sbmt() {
        dispatch('message', {
            text: 'sbmt'
        });
    }
</script>
 
<h1>PAGE 1</h1>
<input bind:value={$page1} />
<button on:click={prev}> prev </button>
<button on:click={sbmt}> submit </button>

