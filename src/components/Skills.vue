<template>
    <div v-for="skill in skills" :key="skill.skillType">
        <p><span class="main-content-heading">{{ skill.skillType }}:</span> <span>{{ skill.skillsList.join(", ") }}</span></p>
        <br>
    </div>
</template>

<script>
export default {
    name: "Skills",
    data() {
        return {
            skills: [
                { skillType: "Languages", skillsList: ["Python", "C", "C++", "Bash", "Java", "HTML", "CSS", "SQL", "RESTful"] },
                { skillType: "Frameworks", skillsList: ["Pytorch", "Tensorflow", "Optuna", "Scikit-Learn", "Pandas", "FastAPI", "Langchain", "Docker", "Scrapy", "Seaborn", "Plotly"] },
                { skillType: "Databases", skillsList: ["MongoDB", "MySQL", "PostgreSQL", "MariaDB", "SkySQL", "CassandraDB", "redis", "DeepLake", "Pinecone"] },
                { skillType: "Tools", skillsList: ["Git", "RPA", "CoPilot", "Obsidian", "Discord", "GitPod"] },
                { skillType: "Platforms", skillsList: ["GitHub", "AWS", "Azure", "Neptune", "Linux", "Firebase", "Tableau", "WnB", "Gradio", "Linux", "Windows", "streamlit", "HuggingFace"]},
                { skillType: "IDE", skillsList: ["VSCode", "IntelliJ Idea", "PyCharm", "Jupyter", "Eclipse", "VIM", "Nano"]},
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../styles/_variables.scss";

.main-content-heading{
    color: $content-heading-color;
}
</style>