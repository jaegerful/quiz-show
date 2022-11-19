<script>
    let seconds = 40

    const timer = () => {
        --seconds

        if (seconds > 0)
            setTimeout(timer, 1000)
    }
</script>

<button on:click = {timer}>00:{(seconds >= 10) ? seconds : `0${seconds}`}</button> 

<style>
    button {
        padding-inline: 1.5em;

        font-weight: 600;
        font-size: 2em;
    }
</style>