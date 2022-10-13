<script>
  import Header from './Header/Header.svelte'
  import Main from './Main.svelte'
  import Footer from './Footer/Footer.svelte'

  let index = 0
</script>

<Header/>

{#key index}
  <Main {index}/>
{/key}

<Footer bind:index/>