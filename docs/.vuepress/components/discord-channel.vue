<template>
    <AutoLink
        :item="{
            link: `https://discordapp.com/channels/${variables.discord.id}/${variables.discord.channels[channel]}`,
            text: `#${channel}`,
        }"
    />
</template>

<script setup lang="ts">
import { defineProps, toRefs } from 'vue';

import AutoLink from '@theme/AutoLink.vue';

const variables = __VAR__;

const props = defineProps({
    channel: {
        type: String,
        required: true,
    },
});

const { channel } = toRefs(props);
</script>
