<script lang="ts">
    import logo from "$lib/assets/logo-v2.svg";
    import Header from "$lib/components/Header.svelte";
    import "../app.css";

    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={logo} />
    <title>etheralinks</title>
</svelte:head>

<div class="font-nohemi font-normal">
    <Header/>
    {@render children()}
</div>
