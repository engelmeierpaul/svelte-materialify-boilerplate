<script lang="ts">
    import {MaterialApp} from 'svelte-materialify';
    import Switch from 'svelte-materialify/src/components/Switch';

    let darkmode = true;
    $: theme = darkmode ? 'dark' : 'light';
</script>

<MaterialApp {theme}>
  <main>
    <h1>Svelte+Materialify!</h1>
    <Switch class="justify-center" color="red" bind:checked={darkmode} inset>Dark Mode</Switch>
    <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
    <p>Visit the <a href="https://svelte-materialify.vercel.app/">Materialify Website</a> to learn about Materialify and
      its components.</p>
  </main>
</MaterialApp>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  div {
    background-color: #00acc1 !important;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
