<script setup lang="ts">
interface Props {
    href?: string;
    color?: string;
}

defineProps<Props>();
</script>

<template>
    <component
        :is="href ? 'a' : 'div'"
        :class="`button ${color ? 'b-' + color + ' ' + color : ''}`"
    >
        <slot></slot>
    </component>
</template>

<style scoped>
.button {
    display: block;
    width: 100%;
    text-decoration: none;
    padding: 1em;
    margin-bottom: 0.75em;
    border: 1px solid var(--color-primary);
    border-radius: 0.5em;
    background-color: var(--background);
    cursor: pointer;
    font-size: 1.333em;
}

.button:hover {
    background-color: var(--background-secondary);
}
</style>
