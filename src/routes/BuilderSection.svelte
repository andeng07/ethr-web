<script lang="ts">
    import Button from "$lib/components/Button.svelte";
    import builderImage from "$lib/assets/mock-builder-1.png";
    import charmImage from "$lib/assets/mock-featured-product-1.png";
</script>

<section class="px-6 py-18">
    <div class="mx-auto flex w-full max-w-6xl flex-col items-start gap-10 md:flex-row md:items-start gap-6">
        <!-- Images -->
        <div class="flex min-w-0 w-full flex-1 gap-1">
            <img
                class="min-w-0 flex-1 object-cover"
                src={builderImage}
                alt="Bracelet builder"
            />

            <img
                class="min-w-0 flex-1 object-cover"
                src={charmImage}
                alt="Featured charm"
            />
        </div>

        <!-- Content -->
        <div class="w-full shrink-0 md:w-fit md:sticky md:top-6 flex flex-col gap-9">
            <div class="flex flex-col gap-1">
                <h1 class="text-5xl">
                    Wear Your Story
                </h1>

                <p class="text-md text-muted">
                    Curate memories, one link at a time.
                </p>
            </div>

            <Button
                href="#"
                label="BUILD YOUR BRACELET"
            />
        </div>

    </div>
</section>
