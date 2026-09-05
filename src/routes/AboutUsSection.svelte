<script lang="ts">
    import { navigation } from "$lib/config/navigation";
    import logo from "$lib/assets/logo-v1.svg";
    import Button from "$lib/components/Button.svelte";

    var aboutUsLink: string = "about"; // todo: retrieve from navigation above
</script>

<section class="py-18 px-6">
    <div class="w-full flex flex-col justify-center items-center gap-24">
        <img src={logo} alt="logo" class="h-16" />
        <h1 class="text-4xl text-center md:text-5xl">always & forever</h1>
        <Button href={aboutUsLink} label="ABOUT US"/>
    </div>
</section>
