<script>
    export let index
    import {questions} from './questions'

    let open = false
    let arrowup = false

    const toggle = () => {
        open = !open
        arrowup = !arrowup
    }
</script>

<main>
    <div id = "question-outer">
        <div id = 'question-inner'>
            <span id = 'question-number'>{`${index + 1}.`}</span>
            <span>{questions[index]['prompt']}</span>
        </div>
    </div>
    <div id = 'answer' class:open>
        <div id = 'header' on:click = {toggle} on:keydown = {toggle}>
            <span id = 'header-text'>Answer:</span>
            <span id = 'arrow' class:arrowup>v</span>
        </div>

        <br>

        <span id = 'answer-text'>
            {questions[index]['answer']}
        </span>
    </div>
</main>

<style>
    main {
        margin-inline: 8vw;
    }

    #question-outer {
        min-height: 30vh;

        border-radius: 0.5em;
        background-color: #1a1a1a;
        padding: 1em 2em;

        font-weight: 500;
        font-size: 3em;

        margin-top: 2vh;
        margin-bottom: 4vh;

        display: flex;
        place-items: center;
    }

    #question-number {
        font-weight: 200;
    }

    #answer {
        border-radius: 0.5em;
        background-color: #1a1a1a;
        padding: 0.6em 2em;

        font-size: 2em;

        height: 2.3em;
        overflow-y: hidden;

        transition: height 0.25s;
    }

    #answer.open {
        height: 6em;
        overflow-y: auto;
    }

    #header {
        display: flex;
        justify-content: space-between;

        transition: border-color 0.25s, color 0.25s;
    }

    #header-text {
        font-weight: 500;
    }

    #arrow {
        transform: translateY(-0.1em) scaleX(1.4);
        transition: transform 450ms ease-out;
    }

    #arrow.arrowup {
        transform: rotate(180deg) scaleX(1.4);
    }

    #header:hover {
        cursor: pointer;

        border-color: #646cff;
        color: #646cff;
    }

    #answer-text {
        font-size: 1.1em;
        color: rgb(204, 165, 37);
    }
</style>