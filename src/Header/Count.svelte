<script>
  let count = 0

  const increment = () => ++count
  const decrement = () => {
    if (count > 0)
      --count
  }
</script>


<div id = 'outer'>
  <button>{count} Points</button>
  
  <div id = 'inner'>
    <button on:click = {increment}>+</button>
    <button on:click = {decrement}>-</button>
  </div>
</div>

<style>
  #outer {
    margin-top: -0.5em;
    margin-left: 0.7em;

    display: inline;
  }

  #outer > button {
    padding: 0.6em 1em;
    
    display: block;
    pointer-events: none;
  }

  #inner {
    margin-top: 0.5em;

    display: flex;
    justify-content: space-around;
  }

  #inner > button {
    padding: 0.1em 1.1em;
    font-size: 0.8em;
  }
</style>