<template>
    <div class="projects">
        <div class="sub-project m-30" v-for="project in projects" :key="project.projectName">
            <p class="main-content-heading">{{ project.projectName }}</p>
            <p> - {{ project.projectDescription }}</p>
            <div v-if="project.githubLink && project.websiteLink">
                <p> - Links: <span> <a :href="project.githubLink" target="_blank">[GitHub]</a> |
                        <a :href="project.websiteLink" target="_blank">[Website]</a></span></p>
            </div>
            <div v-else-if="project.githubLink">
                <p> - Link: <span><a :href="project.githubLink" target="_blank">[GitHub]</a></span></p>
            </div>
            <div v-else-if="project.websiteLink">
                <p> - Link: <span><a :href="project.websiteLink" target="_blank">[Website]</a></span></p>
            </div>
            <p> - Technologies: <span class="color-green">{{ project.tags.join(", ") }}</span></p>
        </div>
    </div>
</template>
  

<script>
export default {
    name: "Projects",
    data() {
        return {
            projects: [
                {
                    projectName: "DROPEX (In Progress)",
                    projectDescription:
                        "A disaster-response and probing technology used for rescuing humans in distress by dropping relief materials with Intelligent Drones.",
                    githubLink: "https://github.com/p1utoze/DROPEX",
                    tags: ["Pytorch", "RaspberryPI", "Shell Script", "AstraDB", "AirSim"],
                },
                {
                    projectName: "Farmsense.ai",
                    projectDescription:
                    "an AI assistant for exponentially growing Hybrid farming.To enhance farmers\textquotesingle{} yield, this application assists them by detecting diseases of plants and poultries and providing crop and egg incubation analysis.",
                    githubLink: "https://tinyurl.com/farmsense-ai",
                    tags: ["Tensorflow", "XGBoost", "Docker", "ReactJS", "FastAPI", "nginx", "AWS EC2"],
                },
                {
                    projectName: "TAP- Test, Apply, Progress",
                    projectDescription: "An AI Platform which provides bilateral service for Job Seekers and Talent Hirers. A dual recommendation system, with Resume parsing and Job post generation model.All models trained on Intel OneAPI Platform.",
                    githubLink: "https://tinyurl.com/tap-ai",
                    websiteLink: "https://weatherlycloud.netlify.app/",
                    tags: ["BeautifulSoup", "Spacy/NLTK", "Intel One-API", "Bash Script"]
                },
                {
                    projectName: "Weather Agent",
                    projectDescription: "A full-stack application built using ReactJS and FastAPI to monitor and generate notification by FetchAI's micro AI Agents.. This application was created as a challenge for IIT-Bombay Hackfest",
                    githubLink: "https://github.com/p1utoze/weatherAgent",
                    websiteLink: "https://weather-agent-client.vercel.app",
                    tags: ["ReactJS", "uagents", "FastAPI", "github Actions"]
                },
                {
                    projectName: "Awesome Installation scripts",
                    projectDescription: "A collaborative project designed to improve the UI of GMU's course registration website",
                    githubLink: "https://github.com/p1utoze/awesome-installation.git",
                    tags: ["Markdown", "Bash", "python"]
                },
            ],
        }
    }
}
</script>

<style scoped lang="scss">
@import "../styles/_variables.scss";

.projects {

    width: 75%;

    & div div {
        margin: 0;
    }

    & .sub-project {
        border-bottom: 2px dashed $grey;
        padding-bottom: 10px;
        margin-bottom: 30px;
    }
}

.main-content-heading{
    color: $content-heading-color;
}

a{
    color: $green;
}
</style>