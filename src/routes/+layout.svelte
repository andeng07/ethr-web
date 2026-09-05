<script lang="ts">
    import logo from "$lib/assets/logo-v2.svg";
    import Footer from "$lib/components/Footer.svelte";
    import Header from "$lib/components/Header.svelte";
    import "../app.css";

    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={logo} />
    <title>ethrealinks</title>
</svelte:head>

<div class="flex min-h-screen flex-col font-nohemi font-normal leading-none max-w-[1920px] m-auto">
    <Header />
    <main class="flex-1">
        {@render children()}
    </main>
    <Footer />
</div>
