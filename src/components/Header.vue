<template>
    <div class="banner-text">
        <p>
            <Prompt /> Loading site...
        </p>
        <p class="m-30">
            <span><a href="https://github.com/p1utoze" target="_blank">Github</a></span> /
            <span><a href="https://www.linkedin.com/in/adithya-awati-87b7541a3/" target="_blank">LinkedIn</a></span> /
            <span><a href="mailto:aditya.n.awati@gmail.com">Email</a></span> /
            <span><a href="https://uploadnow.io/s/b9321c26-4ce3-4ed7-8d87-3206bd4c00b3?o=t"
                    target="_blank">Resume</a></span>
        </p>
    </div>

    <div>
        <img src="../assets/ascii-art.png" alt="Profile" width="500" height="500">
    </div>

    <div class="ascii">
        <h4 style="color: #0fa8cd">Hey, hi, howdyyy! I'm, </h4>
        <pre id="ascii-art">{{ name }}</pre>
        <h4 style="color: #0fa8cd">Welcome to my Linux style terminal portfolio.</h4>
    </div>

    <div class="instructions">
        <p> - Type <span class="main-text">help</span> to see a list of available commands</p>
        <p> - Type <span class="main-text">clear</span> to clear the terminal</p>
        <p> - Use <span class="main-text">up</span> and <span class="main-text">down</span> arrow keys to toggle between
            previous commands</p>
        <p> - Press on <span class="main-text">tab</span> key to auto complete the command</p>
    </div>
</template>
  
<script>
import Prompt from './Prompt.vue';

export default {
    name: "Header",
    components: {
        Prompt
    },
    data() {
        return {
            name: "Error occurred while rendering ascii art",
        };
    },
    mounted() { // Corrected the name of the lifecycle hook to mounted
        try {
            this.name = `
░█████╗░██████╗░██╗████████╗██╗░░██╗██╗░░░██╗░█████╗░  ░█████╗░░██╗░░░░░░░██╗░█████╗░████████╗██╗
██╔══██╗██╔══██╗██║╚══██╔══╝██║░░██║╚██╗░██╔╝██╔══██╗  ██╔══██╗░██║░░██╗░░██║██╔══██╗╚══██╔══╝██║
███████║██║░░██║██║░░░██║░░░███████║░╚████╔╝░███████║  ███████║░╚██╗████╗██╔╝███████║░░░██║░░░██║
██╔══██║██║░░██║██║░░░██║░░░██╔══██║░░╚██╔╝░░██╔══██║  ██╔══██║░░████╔═████║░██╔══██║░░░██║░░░██║
██║░░██║██████╔╝██║░░░██║░░░██║░░██║░░░██║░░░██║░░██║  ██║░░██║░░╚██╔╝░╚██╔╝░██║░░██║░░░██║░░░██║
╚═╝░░╚═╝╚═════╝░╚═╝░░░╚═╝░░░╚═╝░░╚═╝░░░╚═╝░░░╚═╝░░╚═╝  ╚═╝░░╚═╝░░░╚═╝░░░╚═╝░░╚═╝░░╚═╝░░░╚═╝░░░╚═╝
        `;
        } catch (error) {
        }
    }
};
</script>


  
<style lang="scss" scoped>
@import "../styles/_variables.scss";

.main-text {
    color: $primary-color;
}

.name div {
    width: 10px;
}

.ascii,
.ascii-art {
    font-size: 16px;
    line-height: 1.25;
    margin: 30px 0px;
}
</style>
  