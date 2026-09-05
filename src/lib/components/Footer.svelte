<script lang="js">
    import { navigation, socials } from "$lib/config/navigation";
</script>

<footer class="p-6 bg-ink text-muted">
    <div class="w-full flex flex-col justify-center items-center gap-16 lg:gap-32">
        <div><!-- Filler Div --></div>

        <div>
            <h1 class="text-8xl">©ETHR.</h1>
        </div>

        <div class="flex w-full flex-col items-center justify-center gap-8 text-md lg:flex-row">
            <div class="flex w-full flex-row justify-center lg:w-1/3 lg:justify-start">
                <p>©2026</p>
            </div>

            <div class="flex w-full flex-row justify-center lg:w-1/3">
                <nav class="flex flex-row gap-6 lg:gap-16">
                    {#each navigation as link}
                        <a
                            href={link.href}
                            class="text-md hover:text-cream"
                        >
                            {link.label}
                        </a>
                    {/each}
                </nav>
            </div>

            <div class="flex w-full flex-row justify-center lg:w-1/3 lg:justify-end">
                <nav class="flex flex-row gap-6">
                    {#each socials as social}
                        <a
                            href={social.href}
                            class="text-md hover:text-cream"
                        >
                            {social.label}
                        </a>
                    {/each}
                </nav>
            </div>
        </div>
    </div>
</footer>
