<template>
    <div class="m-30" v-for="edu in eduction" :key="edu.institution">
        <p class="main-content-heading">{{ edu.institution }}</p>
        <p>{{ edu.degree }} | {{ edu.dateRange }}</p>
    </div>
</template>

<script>
export default {
    name: "Education",
    data() {
        return {
            eduction: [
                { institution: "The Coding School", degree: "Quantum Computing- QubitxQubit", dateRange: "2023 ~ 2024" },
                { institution: "Dayananda Sagar College of Engineering", degree: "Bachelor of Engineering- AIML", dateRange: "2021 ~ 2025" }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../styles/_variables.scss";

.main-content-heading{
    color: $content-heading-color;
    text-shadow: 0 0 3.5px $content-heading-color;
}

</style>