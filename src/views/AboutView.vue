<template>
    <div class="about">
        <template v-if="selectedSport === 'Tennis'">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1296.28 741.28">
                <CourtBuilderBase />
                <TennisPlayingArea :areaColor="tennisPlayingAreaColor" />
                <TennisBoundryLines :lineColor="tennisBoundaryLineColor" />
                <TennisNet />
            </svg>
        </template>


        <div v-if="selectedSport === 'Tennis'">
            <label>
                Tennis Playing Area Color:
                <select v-model="tennisPlayingAreaColor">
                    <option v-for="group in colorOptions" :key="group.label">
                        <optgroup :label="group.label">
                            <option v-for="color in group.options" :value="color.value" :key="color.label">
                                {{color.label}}
                            </option>
                        </optgroup>
                    </option>
                </select>
            </label>

            <label>
                Tennis Boundary Lines Color:
                <select v-model="tennisBoundaryLineColor">
                    <option v-for="group in colorOptions" :key="group.label">
                        <optgroup :label="group.label">
                            <option v-for="color in group.options" :value="color.value" :key="color.label">
                                {{color.label}}
                            </option>
                        </optgroup>
                    </option>
                </select>
            </label>
        </div>

    </div>
</template>

<script lang="ts">
    import { defineComponent, ref } from "vue";
    import CourtBuilderBase from '@/components/layout/CourtBuilderBase.vue';
    import TennisPlayingArea from '@/components/layout/tennis/TennisPlayingArea.vue';
    import TennisBoundryLines from '@/components/layout/tennis/TennisBoundryLines.vue';
    import TennisNet from '@/components/layout/tennis/TennisNet.vue';

    export default defineComponent({
        name: "CourtDesigner",
        components: {
            CourtBuilderBase,
            TennisPlayingArea,
            TennisBoundryLines,
            TennisNet,
        },
        setup() {
            const selectedSport = ref('Tennis');
            const overlayBasketball = ref(false);
            const overlayTennis = ref(false);

            const tennisPlayingAreaColor = ref('#445f43');
            const tennisBoundaryLineColor = ref('#FFFFFF');

            const colorOptions = [
                {
                    label: 'Player’s Choice Colors',
                    options: [
                        { label: 'Brilliant White', value: '#fff' },
                        { label: 'Competition Green', value: '#445f43' },
                        { label: 'Pro Green', value: '#475b3f' },
                        { label: 'Medium Green', value: '#3d4933' },
                        { label: 'Forest Green', value: '#444b3e' },
                        { label: 'Slate', value: '#525456' },
                        { label: 'Gray', value: '#6c6d6f' },
                        { label: 'Competition Blue', value: '#1a3054' },
                        { label: 'Standard Blue', value: '#233e6d' },
                        { label: 'Pro Blue', value: '#1b3d5c' },
                        { label: 'Light Blue', value: '#23548c' },
                        { label: 'Sandstone', value: '#8c7f6e' },
                        { label: 'Beige', value: '#8e7053' },
                        { label: 'Terra Cotta', value: '#966b53' },
                        { label: 'Standard Orange', value: '#a8593f' },
                        { label: 'Classic Red', value: '#7b3522' }
                    ]
                },
                {
                    label: 'Specialty Colors',
                    options: [
                        { label: 'Sky Blue', value: '#82a3d5' },
                        { label: 'Caribbean Blue', value: '#3474a4' },
                        { label: 'Sea Green', value: '#347481' },
                        { label: 'Nautical Navy', value: '#111f2c' },
                        { label: 'Pro Purple', value: '#3f3c5e' },
                        { label: 'Ultra Violet', value: '#542f7e' },
                        { label: 'Viva Violet', value: '#874d97' },
                        { label: 'Crimson', value: '#702c32' },
                        { label: 'Bright Red', value: '#9e2b32' },
                        { label: 'Passion Pink', value: '#e15d96' },
                        { label: 'Coral', value: '#ec6661' },
                        { label: 'Bright Orange', value: '#df7e3b' },
                        { label: 'Bright Yellow', value: '#f3bb47' },
                        { label: 'Kiwi', value: '#79a448' },
                        { label: 'Lime', value: '#5fac45' }
                    ]
                }
            ];

            return {
                selectedSport,
                overlayBasketball,
                overlayTennis,
                tennisPlayingAreaColor,
                tennisBoundaryLineColor,
                colorOptions
            };
        }
    });
</script>

<style scoped>
    .about {
        position: relative;
    }
</style>