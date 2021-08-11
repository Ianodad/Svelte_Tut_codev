<script>
    import {onMount} from 'svelte'

    let inputRef

    onMount(() => {
        imputRef.focus()
    })
</script>

<input type="text" bind:this={inputRef}>