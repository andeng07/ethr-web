<script lang="ts">
    import productImage from "$lib/assets/mock-featured-product-1.png";
    import productImageV2 from "$lib/assets/mock-featured-product-2.png";
    import Button from "$lib/components/Button.svelte";
</script>

<section
    class="grid w-full overflow-hidden md:grid-cols-2 md:aspect-2/1 md:max-h-180"
>
    <div
        class="flex min-h-120 flex-col items-center justify-center gap-6 bg-cream p-6 md:min-h-0"
    >
        <img
            class="max-h-80 max-w-full object-contain md:max-h-[55%]"
            src={productImage}
            alt="The Marquise Link"
        />

        <div
            class="flex flex-col items-center justify-center gap-16 text-center"
        >
            <div>
                <h1 class="text-2xl">The Marquise Link</h1>
                <p class="max-w-md text-[16px] text-muted md:text-[18px]">
                    A sculptural piece designed to hold a moment
                </p>
            </div>
            <Button href="#" label="VIEW PRODUCT" />
        </div>
    </div>

    <div class="hidden overflow-hidden bg-muted md:flex">
        <img
            class="h-full w-full object-cover"
            src={productImageV2}
            alt="The Marquise Link lifestyle"
        />
    </div>
</section>
