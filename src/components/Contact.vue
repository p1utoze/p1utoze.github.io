<template>
    <div v-for="contact in contactInfo" :key="contact.contactName">
        <p><span class="main-content-heading">[{{ contact.contactName }}]</span>: <span><a target="_blank" :href="getContactLink(contact)">{{ contact.contactLink }}</a></span></p>
    </div>
</template>

<script>
export default {
    name: "Contact",
    data() {
        return {
            contactInfo: [
                { contactName: "Email", contactLink: "aditya.n.awati@gmail.com" },
                { contactName: "Github", contactLink: "https://github.com/p1utoze" },
                { contactName: "LinkedIn", contactLink: "https://www.linkedin.com/in/adithya-awati-87b7541a3/" },
                { contactName: "Kaggle", contactLink: "https://www.kaggle.com/adithyaawati"},
                { contactName: "Resume", contactLink: "https://uploadnow.io/s/b9321c26-4ce3-4ed7-8d87-3206bd4c00b3?o=t" },
            ],
        };
    },
    methods: {
        getContactLink(contact) {
            if (contact.contactName === "Email") {
                return "mailto:" + contact.contactLink;
            }
            return contact.contactLink;
        },
    },
};
</script>

<style lang="scss" scoped>
@import "../styles/_variables.scss";

.main-content-heading{
    color: $content-heading-color;
    text-shadow: 0 0 5px $content-heading-color;
}

</style>
