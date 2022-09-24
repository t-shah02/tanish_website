<script>
    export let images = [];
    export let title = "Project";
    export let actions = [];
    export let links = {};
    export let description = "Description";
    export let techStack = [];


    const goLeft = () => {
        sliderIndex--;
        if (sliderIndex < 0) {
            sliderIndex = images.length - 1;
        }
    }

    const goRight = () => {
        sliderIndex++;
        if (sliderIndex >= images.length) {
            sliderIndex = 0;
        }
    }

    const openImageInNewTab = () => {
        window.open(images[sliderIndex],"_blank");
    }

    const DEV_ICON_MAP = {
        github: "devicon-github-original",
        devpost: "fa-brands fa-dev",
        youtube: "fa-brands fa-youtube",
        discord : "fa-brands fa-discord"
    };

    let sliderIndex = 0;
</script>

<div class="card">
    <h1 class="title">{title}</h1>
    <h2 style="text-align:center; font-style : italic; font-size : 14px">Click on the images to view them in a new tab!</h2>
    <div
        on:click={openImageInNewTab}
        style="background-image : url('{images[sliderIndex]}')"
        class="gallery"
    />
    <div class="bottom-panel">
        <div class="links">
            {#each Object.entries(links) as [platform, linkURL]}
                <a href={linkURL} target="_blank">
                    <i class={DEV_ICON_MAP[platform]} />
                </a>
            {/each}
        </div>
        
        {#if images.length >= 2}
            <div class="gallery-controls">
                <h2 class="image-number">{sliderIndex + 1} / {images.length}</h2>
                <button on:click={goLeft} class="left control-btn"> ← </button>
                <button on:click={goRight} class="right control-btn"> → </button>
            </div>
        {/if}
    </div>
    <h2>Tech Stack 🍔:
        <span>
            {techStack.join(", ")}
        </span> 
    </h2>
    <hr class="divider">
    <p>
        {description}
    </p>
</div>

<style>
    .card {
        display: block;
        margin-left: auto;
        margin-right: auto;
        width: 95%;
        margin: 15px;
        margin-bottom : 25px;
    }

    p {
        margin-top : 5px;
    }

    .image-number {
        font-size : 15px;
        margin-right : 7px;
        margin-top : 5px;
    }

    .bottom-panel {
        width : 100%;
        display : flex;
        align-items : center;
        margin-top : 7.5px;
    }

    .gallery-controls {
        display: flex;
        align-items: center;
        margin-left : auto;
    }

    .links > a {
        display :inline-block;
        transform : scale(1.5);
        margin : 8px;
    }

    .gallery {
        margin-top: 10px;
        height: 450px;
        background-repeat : no-repeat;
        background-size : cover;
        background-position : center;
        border-radius: 10px;
        box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
        transition : all 100ms ease-in-out;
    }


    .gallery:hover {
        cursor : pointer;
        transform : scale(1.01);
    }

    .control-btn {
        margin: 5px;
        padding: 3.5px;
        font-size: 20px;
        color: white;
        background-color: #4ee44e;
        border: none;
        border-radius: 5px;
    }

    .control-btn:hover {
        cursor: pointer;
    }

    i {
        color : black;
    }

    .title {
        font-size: 18px;
        text-align: center;
    }

    h2 {
        font-size : 15px;
        margin-bottom : 8.5px;
    }

    h2 span {
        color : grey;
    }

    .divider { 
        border : 1px solid black;
    }

</style>
