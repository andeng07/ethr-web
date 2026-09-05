<script lang="ts">
    import { setContext } from "svelte";

    let open = $state(false);

    setContext("accordion-item", {
        get open() {
            return open;
        },
        toggle() {
            open = !open;
        }
    });

    let { children } = $props();
</script>

<div class="w-full flex flex-col border-b-2 border-b-muted pb-4">
    {@render children()}
</div>
