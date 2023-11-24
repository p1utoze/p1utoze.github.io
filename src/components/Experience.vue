<template>
    <div class="generate-exp">
        <div class="work" v-for="exp in experience" :key="exp.company">
            <p class="main-content-heading">{{ exp.position }} @ {{ exp.company }}</p>
            <p>- {{ exp.dateRange }}</p>
            <p>- {{ exp.location }}</p>
            <div class="work-content" v-for="content in exp.content" :key="content" style="margin: 0;">
                <p>- {{ content }}</p>
            </div>
        </div>
    </div>
</template>
  
<script>
export default {
    name: "Experience",
    data() {
        return {
            experience: [
                {
                    company: "CellStrat AI",
                    position: "Machine Learning Intern",
                    location: "Bengaluru, India",
                    dateRange: "Dec. 2022 - Feb. 2023",
                    content: [
                        "Leveraged cloud-based platform to develop and deploy machine learning models efficiently",
                        "Designed and implemented inference endpoints using RESTful APIs services on the platform seamlessly.",
                        "Built robust machine learning models for consumer complaint classification and customer lifetime value prediction, enhancing customer experience and marketing strategies."                    ]
                }
            ]
        };
    }
};
</script>


<style scoped lang="scss">
@import "../styles/_variables.scss";
.work{
    padding-bottom: 10px;
    margin-bottom: 30px;
    border-bottom: 2px dashed $grey;
}

.main-content-heading{
    color: $content-heading-color;
    text-shadow: 0 0 3.5px $content-heading-color;
}

.generate-exp{
    width: 75%;
}
</style>