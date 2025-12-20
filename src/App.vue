<script setup lang="ts">
import { ref, onMounted } from "vue";
import LucideIcon from "./components/LucideIcon.vue";
import CustomButton from "./components/CustomButton.vue";

const visible = ref<boolean>(false);

onMounted(() => {
    setTimeout(() => {
        visible.value = true;
    });
});
</script>

<template>
    <main :style="{ display: visible ? 'inherit' : 'none' }">
        <!-- TODO: 1. rename app -->
        <h1>
            <LucideIcon name="package" />
            Vue-Boilerplate
        </h1>
        <br />
        <p>
            Fill this page with <i>whatever</i> you're going to develop.
            <br />
            <b>Then enjoy!</b>
        </p>
        <CustomButton>
            <LucideIcon name="square-arrow-right" /> This is a sample button yay
        </CustomButton>
        <br />
        <hr />
        <small class="footer">
            <LucideIcon name="at-sign" />
            &nbsp;
            <a href="https://github.com/klemek" target="_blank">klemek</a>
            -
            <!-- TODO: 1. rename app -->
            <LucideIcon name="github" />
            &nbsp;
            <a href="https://github.com/klemek/vue-boilerplate" target="_blank">
                Repository
            </a>
            - 2025
        </small>
    </main>
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

.footer {
    opacity: 50%;
}
</style>
