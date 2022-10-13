<script>
    import Count from './Count.svelte'
</script>

<header>
    <div>Kids: <Count/></div>
    <div>Adults: <Count/></div>
</header>

<style>
    header {
        padding: 3em;

        display: flex;
        justify-content: space-between;
    }

    div {
        font-size: 2em;
        display: flex;
    }
</style>