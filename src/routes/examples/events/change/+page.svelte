<script>
    import Select from '$lib/Select.svelte';

    let items = [
        { value: 'one', label: 'One' },
        { value: 'two', label: 'Two' },
        { value: 'three', label: 'Three' },
    ];

    function handle(selectedValue) {
        console.log('You change the svelte select 🤯 ', $state.snapshot(selectedValue));
    }
</script>

<Select {items} onchange={handle} />
