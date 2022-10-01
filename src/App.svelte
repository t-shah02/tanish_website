
<script>
    
    import AboutModal from "./components/AboutModal.svelte";  
    import ProjectsModal from "./components/ProjectsModal.svelte";


    // state variables
    let aboutActive = false;


    const openResume = () => window.open("/static/misc/resume.pdf","_blank");
    


</script>

<div class="content-card">
    <div class="basic-me">
        <h1>Tanish Shah</h1>
        <h2>Data Science student @ Simon Fraser University</h2>
        <h2>Love Full Stack and Big Data Dev</h2>
        <h2>Seeking Co-ops and Internships for Spring 2023</h2>
        <div class="contact-icons">
            <a target="_blank" href="https://github.com/t-shah02">
                <i class="fa-brands fa-github" />
            </a>
            <a
                target="_blank"
                href="https://www.linkedin.com/in/tanish-shah-888121210/"
            >
                <i class="fa-brands fa-linkedin" />
            </a>
            <a target="_blank" href="mailto:tanish_shah@sfu.ca">
                <i class="fa-solid fa-envelope" />
            </a>
        </div>
    </div>
    <hr />

    <AboutModal/>
    <ProjectsModal/>

    <div class="controls">
        <button data-hystmodal="#about-modal">About</button>
        <button data-hystmodal="#projects-modal">Projects</button>
        <button on:click={openResume}>Resume</button>

    </div>
    <img alt="tanish shah" src="/static/home/tanish.jpg" />
    
</div>
