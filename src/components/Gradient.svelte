<script>
    import { onMount } from 'svelte'

    onMount(() => {
        const projectsParent = document.querySelector(".hero");
        const projectsCard = document.querySelectorAll(".heroImage");

        projectsParent.addEventListener("pointermove", (ev) => {
            projectsCard.forEach((project) => {
                const rect = project.getBoundingClientRect();

                project.style.setProperty("--x", ev.clientX - rect.left);
                project.style.setProperty("--y", ev.clientY - rect.top);

            });
        });
    })
</script>
<div class="hero">
    <div class="gradient">
        <div class="gradientBackground">
            <div class="side right"></div>
            <div class="side left"></div>
            <div class="heroImage" style="">
                <video alt="The MechaKeys application running on Windows" class="appphoto" src="../images/appvideo.mp4" autoplay="true" muted="" loop="true" sstyle="filter: hue-rotate(0deg) !important; animation: none !important;"></video>
            </div>
        </div>
    </div>
</div>

<style>
.appphoto {
    border-radius: 1rem;
    opacity: 0.95;
}
.side.left:hover ~ .heroImage .appphoto {
    transition: 600ms ease;
    transform: matrix3d(1, 0, 0.01, -0.00002, 0, 1, 0, 0, -0.7, 0, 0.1, 0, 1, 1, 10, 0.9);
    box-shadow: 0 0 8rem #00000080;
    opacity: 1;
}

.side.right:hover ~ .heroImage .appphoto {
    transition: 600ms ease;
    transform: matrix3d(1, 0, -0.01, 0.00002, 0, 1, 0, 0, -0.7, 0, 0.1, 0, 1, 1, 10, 0.9);
    box-shadow: 0 0 8rem #00000080;
    opacity: 1;
}

.appphoto {
    transition: 600ms ease;
}

.appphoto {
    width: 100%;
}

.side {
    position: absolute;
    width: 50%;
    top: 0;
    bottom: 0;
    z-index: 10;
}
.side.right {
  right: 0
}

.side.left {
  left: 0;
}
.hero {
    height: 100vh;
    display: flex;
    flex: 1;
}

.gradient {
    position: relative;
    width: 100%;
    height: 100%;
    overflow: hidden;
    border-radius: 0px 0px 00px 50px
}

.gradientBackground {
    position: absolute;
    display: flex;
    align-items: center;
    justify-content: center;
    
    border-radius: 0px 0px 0px 50px;
    width: 100%;
    min-height: calc(100% - 15%);
}

.gradientBackground::before {
    width: 100%;
    height: 100%;
    content: "";
    position: absolute;
    border-radius: inherit;
    animation: gradientHue 5s ease-in-out infinite forwards;
    background: radial-gradient(165.15% 212.12% at 116.37% -18.44%, #A2AAF4 0%, #66F9B2 0%, #8F97FF 35.05%, #877EF5 48.44%, #CF7CDC 70.02%, #EC63CE 100%) /* warning: gradient uses a rotation that is not supported by CSS and may not behave as expected */;
}

.heroImage {
    animation: 500ms linear 0s 1 normal backwards running blur-in;
    animation-delay: 300ms;
    display: flex;
    flex-shrink: 1;
    transition: 600ms ease;
    margin: 2rem;
    width: 750px;
    border-radius: 0.75rem;

    perspective: 200px;
    transition: all 0.2s ease;
}

.heroImage:hover {
    /* transform: scale(1.05); */
    transition: 600ms ease;
}

@keyframes blur-in {
    0% {
        opacity:0;
        -webkit-filter:blur(70px);
        filter:blur(70px);
    }
    70% {
        -webkit-filter:none;
        filter:none;
    }
    100% {
        opacity:1;
        -webkit-filter:none;
        filter:none;
    }
}

@keyframes gradientHue {
    0% {
        filter: hue-rotate(0deg)
    }

    25% {
        filter: hue-rotate(45deg)
    }

    50% {
        filter: hue-rotate(90deg)
    }

    75% {
        filter: hue-rotate(45deg)
    }

    100% {
        filter: hue-rotate(0deg)
    }
    
}

/* @media only screen and (max-width: 800px) {
    .gradient, .gradientBackground {
        border-radius: 0 !important;
    }

    .heroImage {
        display: flex;
    }
} */

@media only screen and (max-width: 800px) {
    .gradient, .gradientBackground {
        border-radius: 0 !important;
        height: 500px !important;
    }
}
</style>