<script lang="ts">
    import { getContext } from "svelte";
    import { ArrowDownRight } from "@lucide/svelte";
    import type { Snippet } from "svelte";

    let { children }: { children: Snippet } = $props();

    const accordion = getContext<{
        readonly open: boolean;
        toggle: () => void;
    }>("accordion-item");
</script>

<button
    class="group w-full flex flex-row items-center gap-1
           hover:cursor-pointer
           transition-[gap] duration-300 ease-out
           hover:gap-4"
    class:gap-4={accordion.open}
    onclick={accordion.toggle}
>
    <p class="text-3xl md:text-4xl">
        {@render children()}
    </p>

    <ArrowDownRight
        size={36}
        class="opacity-25
               transition-all duration-300 ease-out
               group-hover:opacity-100
               {accordion.open ? '-rotate-90 opacity-100' : ''}"
    />
</button>
