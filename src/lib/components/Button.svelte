<script lang="ts">
    let { href, label }: { href: string; label: string } = $props();
</script>

<div>
    <a {href} class="border-b border-b-muted text-md text-muted hover:border-b-blue hover:text-blue">
        {label}
    </a>
</div>
