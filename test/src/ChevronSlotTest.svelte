<script>
    import Select from '../../src/lib/Select.svelte';

    let items = $state(['one', 'two']);
    let value = $state();
    let listOpen = $state(true);
</script>

<Select bind:items bind:value bind:listOpen showChevron>
    {#snippet chevronIconSnippet(listOpen)}
        {#if listOpen}
            ⬆️
        {:else}
            ⬇️
        {/if}
    {/snippet}
</Select>
