<template>
    <app-layout>
        <template #header>Tooltips</template>
        <template #subHeader>Smart and fast infos in the line</template>
        <template #default>
            <grid-section :col="1" :gap="4">
                <t-content-card :width="1">
                    <template #title>Simple</template>
                    <template #subTitle>Left, Top, Right and Bottom Positions</template>
                    <template #content>
                        <div class="flex flex-wrap space-x-8">
                            <t-tooltip position="top">
                                <template #mainContent>Hover me!</template>
                                <template #secondContent>Hello, I'm at the top</template>
                            </t-tooltip>
                            <t-tooltip position="bottom">
                                <template #mainContent>Hover me!</template>
                                <template #secondContent>Hello, I'm at the bottom</template>
                            </t-tooltip>
                            <t-tooltip position="left">
                                <template #mainContent>Hover me!</template>
                                <template #secondContent>Hello, I'm at the left</template>
                            </t-tooltip>
                            <t-tooltip position="right">
                                <template #mainContent>Hover me!</template>
                                <template #secondContent>Hello, I'm at the right</template>
                            </t-tooltip>
                        </div>
                    </template>
                </t-content-card>
            </grid-section>
        </template>
    </app-layout>
</template>

<script>
/*Layout*/
import AppLayout from "@/Layouts/AppLayout";
/*Component*/
import GridSection from "@/Layouts/GridSection";
import TContentCard from "@/Components/Card/TContentCard";
import TTooltip from "@/Components/Tooltip/TTooltip";

export default {
    name: "Tooltip",
    components: {AppLayout, GridSection, TContentCard, TTooltip},
}
</script>

<style scoped>

</style>
