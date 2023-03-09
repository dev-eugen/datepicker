<template>
    <div class="wrapper">
        <Datepicker
v-model="selectedDate"  :markers=" [
                {
                    date: addDays(new Date(), 1),
                    type: 'dot',
                    tooltip: [{ text: 'Dot with tooltip', color: 'green' }],
                },
                {
                    date: addDays(new Date(), 2),
                    type: 'dot',
                    tooltip: [
                        { text: 'First tooltip', color: 'blue' },
                        { text: 'Second tooltip', color: 'yellow' },
                    ],
                },
                {
                    date: addDays(new Date(), 3),
                    type: 'dot',
                    color: 'yellow',
                },
            ]"
            placeholder="Select Date"
        />
    </div>
</template>

<script lang="ts" setup>
    import { ref } from 'vue';
    import Datepicker from '../src/VueDatePicker/VueDatePicker.vue';
    import addDays from 'date-fns/addDays';

    const selectedDate = ref();
</script>

<style lang="scss">
    @import 'src/VueDatePicker/style/main';
    .wrapper {
        padding: 100px;
    }
</style>
