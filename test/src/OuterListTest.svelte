<script>
    import Select from '../../src/lib/Select.svelte';

    let items = $state(['one', 'two']);
    let value = $state('one');
</script>

<Select bind:items bind:value listOpen>
    {#snippet listPrependSnippet()}
        prepend
    {/snippet}

    {#snippet listAppendSnippet()}
        append
    {/snippet}
</Select>
