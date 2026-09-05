<script lang="ts">
    import { Handbag, Menu, X, ArrowRight } from "@lucide/svelte";
    import { navigation } from "$lib/config/navigation";
    import logo from "$lib/assets/logo-v1.svg";
    import { slide } from "svelte/transition";

    let bagCount: number = $state(0);
    let menuOpen = $state(false);
</script>

<header class="relative w-full bg-cream">
    <!-- Header -->
    <div class="relative flex h-16 items-center px-6">
        <!-- Navigation -->
        <div class="flex w-1/3 items-center justify-start">
            <!-- Desktop -->
            <nav class="hidden flex-row gap-9 md:flex">
                {#each navigation as link}
                    <a
                        href={link.href}
                        class="text-md transition-opacity duration-200 hover:text-muted"
                    >
                        {link.label}
                    </a>
                {/each}
            </nav>

            <!-- Mobile -->
            <button
                type="button"
                class="md:hidden hover:cursor-pointer"
                aria-label={menuOpen ? "Close navigation" : "Open navigation"}
                aria-expanded={menuOpen}
                onclick={() => (menuOpen = !menuOpen)}
            >
                {#if menuOpen}
                    <X size={24} strokeWidth={2} />
                {:else}
                    <Menu size={24} strokeWidth={2} />
                {/if}
            </button>
        </div>

        <!-- Logo -->
        <div class="flex w-1/3 justify-center">
            <a href="/">
                <img src={logo} alt="ethrlinks" />
            </a>
        </div>

        <!-- Bag -->
        <div class="flex w-1/3 justify-end">
            <a
                href="/bag"
                class="group flex flex-row items-center gap-2 hover:text-muted"
            >
                <Handbag size={20} strokeWidth={2} />

                <span class="flex flex-row gap-1 text-sm">
                    <span class="hidden sm:inline">Bag</span>
                    <span>({bagCount})</span>
                </span>
            </a>
        </div>
    </div>

    {#if menuOpen}
        <nav
            class="absolute left-0 top-full z-50 w-full overflow-hidden border-t border-black/10 bg-cream px-6 py-7 md:hidden"
        >
            <div class="flex flex-col" transition:slide={{ duration: 250 }}>
                {#each navigation as link, i}
                    <a
                        href={link.href}
                        onclick={() => (menuOpen = false)}
                        class="group flex items-center justify-between border-b border-black/10 py-4 first:pt-0"
                    >
                        <span
                            class="text-4xl tracking-tight transition-transform duration-200 group-hover:translate-x-1"
                        >
                            {link.label}
                        </span>

                        <span
                            class="opacity-30 transition-all duration-200 group-hover:translate-x-1 group-hover:opacity-70"
                        >
                            <ArrowRight/>
                        </span>
                    </a>
                {/each}
            </div>
        </nav>
    {/if}
</header>
