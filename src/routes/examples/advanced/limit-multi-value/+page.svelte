<script>
    import Select from '$lib/Select.svelte';

    const _items = [
        { value: 'one', label: 'One' },
        { value: 'two', label: 'Two' },
        { value: 'three', label: 'Three' },
        { value: 'four', label: 'Four' },
        { value: 'five', label: 'Five' },
        { value: 'six', label: 'Six' },
    ];

    let value = $state();

    let maxItems = $derived(value?.length === 4);
    let items = $derived(maxItems ? [] : [..._items]);
</script>

<Select {items} multiple bind:value>
    {#snippet emptySnippet()}
        <div class="empty">{maxItems ? 'Max 4 items' : 'No options'}</div>
    {/snippet}
</Select>

<style>
    .empty {
        text-align: center;
        padding: 20px 0;
    }
</style>
