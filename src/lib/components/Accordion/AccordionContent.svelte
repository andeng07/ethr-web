<script lang="ts">
    import { getContext } from "svelte";
    import { slide } from "svelte/transition";
    import type { Snippet } from "svelte";

    let { children }: { children: Snippet } = $props();

    const accordion = getContext<{
        readonly open: boolean;
    }>("accordion-item");
</script>

{#if accordion.open}
    <div
        class="w-full py-4"
        transition:slide={{ duration: 300 }}
    >
        {@render children()}
    </div>
{/if}
