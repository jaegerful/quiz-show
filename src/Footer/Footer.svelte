<script>
    import Time from './Time.svelte'
    export let index

    const increment = () => ++index
    const decrement = () => {
        if (index > 0)
        --index
    }
</script>

<div>
    <button on:click = {decrement}>&lt;</button>

    {#key index}
        <Time/>
    {/key}
    
    <button on:click = {increment}>&gt;</button>
</div>

<style>
    div {
        width: 100%;

        display: flex;
        justify-content: space-around;

        position: fixed;
        bottom: 0;

        margin-bottom: 5vh;
    }

    button {
        padding: 0.2em 1em;

        font-weight: 900;
        font-size: 2.5em;
    }
</style>