<script lang="ts">
    import Accordion from "$lib/components/Accordion/Accordion.svelte";
    import AccordionContent from "$lib/components/Accordion/AccordionContent.svelte";
    import AccordionItem from "$lib/components/Accordion/AccordionItem.svelte";
    import AccordionTitle from "$lib/components/Accordion/AccordionTitle.svelte";
    import Button from "$lib/components/Button.svelte";

    import { styles } from "$lib/config/styles";
</script>

<section class="w-full p-6">
    <div class="grid grid-cols-1 gap-6 md:grid-cols-[1fr_auto_2fr] md:items-start md:gap-12">
        <!-- Heading -->
        <div class="flex flex-col items-end gap-2 md:sticky md:top-6 md:items-end">
            <h1 class="text-4xl text-right md:text-5xl">Styles for Every Moment</h1>

            <Button href="/collections" label="ALL STYLES" />
        </div>

        <!-- Divider -->
        <div class="hidden w-1 self-stretch bg-muted md:block"></div>

        <!-- Accordion -->
        <div>
            <Accordion>
                {#each styles as { href, style, description }}
                    <AccordionItem>
                        <AccordionTitle>
                            {style}
                        </AccordionTitle>

                        <AccordionContent>
                            <div class="flex flex-col items-start gap-4">
                                <p class="text-ink leading-[1.5]">
                                    {description}
                                </p>

                                <div class="flex">
                                    <Button {href} label="EXPLORE STYLE" />
                                </div>
                            </div>
                        </AccordionContent>
                    </AccordionItem>
                {/each}
            </Accordion>
        </div>
    </div>
</section>
