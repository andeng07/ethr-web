<script lang="ts">
    import productPreview from "$lib/assets/mock-hero-1.png";
    import Button from "$lib/components/Button.svelte";
</script>

<section
    class="w-full px-5 py-12 pt-14 sm:pt-16 md:px-8 md:pt-20 lg:px-10 xl:px-12"
>
    <div class="mx-auto flex w-full flex-col items-center justify-center">
        <div class="mx-auto w-fit flex flex-col items-center justify-center">
            <!-- ETHR + IMAGE -->
            <div
                class="
                    flex w-fit flex-col items-center justify-center
                    gap-3 sm:gap-4
                    md:flex-row md:gap-2
                "
            >
                <h1
                    class="
                        shrink-0 font-medium leading-[0.7]
                        text-[clamp(72px,17vw,110px)]
                        sm:text-[clamp(80px,15vw,130px)]
                        md:text-[clamp(72px,10.5vw,164px)]
                    "
                >
                    ethr
                </h1>

                <img
                    src={productPreview}
                    alt="product-preview"
                    class="
                        h-auto
                        w-[clamp(140px,35vw,220px)]
                        sm:w-[clamp(180px,35vw,280px)]
                        lg:w-full
                    "
                />
            </div>

            <!-- DESCRIPTION + EALINKS -->
            <div
                class="
                    flex w-full flex-col items-center justify-center
                    gap-4 sm:gap-5
                    md:flex-row md:gap-2
                "
            >
                <!-- DESCRIPTION -->
                <div
                    class="
                        order-2 shrink-0
                        w-[min(280px,80vw)]
                        md:order-1
                        md:w-[clamp(130px,14vw,232px)]
                    "
                >
                    <h2
                        class="
                            text-center leading-none text-blue
                            text-[clamp(13px,3.5vw,16px)]
                            md:text-right
                            md:text-[clamp(12px,1.3vw,20px)]
                        "
                    >
                        Embodies timeless moments,
                        <span class="text-muted">
                            with bespoke charms
                        </span>
                        that unravels your story
                    </h2>
                </div>

                <h1
                    class="
                        order-1 shrink-0 font-medium leading-[0.7] text-muted
                        text-[clamp(72px,17vw,110px)]
                        sm:text-[clamp(80px,15vw,130px)]
                        md:order-2
                        md:text-[clamp(72px,10.5vw,164px)]
                    "
                >
                    ealinks
                </h1>
            </div>
        </div>

        <!-- CTA -->
        <div
            class="
                mt-10 flex w-full justify-center
                sm:mt-12 sm:justify-end
                md:mt-10
            "
        >
            <Button href="#" label="SCROLL TO EXPLORE" />
        </div>
    </div>
</section>
