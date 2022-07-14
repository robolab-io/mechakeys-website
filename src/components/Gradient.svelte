<script>
    import { onMount } from 'svelte'

    onMount(() => {
        const heroParent = document.querySelector(".hero");
        const heroChild = document.querySelectorAll(".spotlight");

        heroParent.addEventListener("pointermove", (ev) => {
            heroChild.forEach((content) => {
                const rect = content.getBoundingClientRect();

                content.style.setProperty("--x", ev.clientX - rect.left);
                content.style.setProperty("--y", ev.clientY - rect.top);
                content.style.setProperty("--degX", ev.clientX * 0.02);
                content.style.setProperty("--degY", ev.clientY * 0.02);
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
                <div class="spotlight"></div>
                <video alt="The MechaKeys application running on Windows" class="appphoto" src="../images/appvideo.mp4" autoplay="true" muted="true" loop="true" style="filter: hue-rotate(0deg) !important; animation: none !important;"></video>
            </div>
        </div>
    </div>
</div>

<style>
.appphoto {
    border-radius: 1rem;
    opacity: 0.89;
    transition: 600ms ease;
    width: 100%;
}
.side.left:hover ~ .heroImage .appphoto {
    transition: 600ms ease;
    transform: matrix3d(1, 0, -0.001, 0.00002, 0, 1, 0, 0, -0.2, 0, 0.1, 0, 1, 1, 10, 1) translateX(-4px); 
    box-shadow: 0 0 2rem #000000e0;
    opacity: 1;
}

.side.right:hover ~ .heroImage .appphoto {
    transition: 600ms ease;
    transform: matrix3d(1, 0, 0.001, -0.00002, 0, 1, 0, 0, -0.2, 0, 0.1, 0, 1, 1, 10, 1)  translateX(4px);
    box-shadow: 0 0 2em #000000e0;
    opacity: 1;
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
    height: 700px;
    display: flex;
    flex: 1;
    animation: 1900ms ease-in 0s 1 normal backwards running blur-in;
}

.gradient {
    position: relative;
    width: 100%;
    height: 100%;
    overflow: hidden;
    border-radius: 50px 00px 00px 50px;
    margin: 4rem 0rem 2rem 2rem;
    
}

.gradientBackground {
    position: absolute;
    display: flex;
    align-items: center;
    justify-content: center;
    
    border-radius: 50px 00px 00px 50px;
    width: 100%;
    min-height: clamp(calc(100% - 45%), calc(100% - 25%), calc(100% - 10%));
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
    animation-delay: 300ms;
    display: flex;
    flex-shrink: 1;
    transition: 600ms ease;
    margin: 2rem;
    width: 750px;
    border-radius: 0.75rem;

    perspective: 1000px;
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
@media only screen and (max-width: 1600px) {

    .heroImage {
        position: absolute;
        left: 0;
    }
}

@media only screen and (max-width: 800px) {
    .gradient, .gradientBackground {
        border-radius: 2rem 2rem 0rem 0rem !important;
        height: 450px !important;
        margin: 0 !important;
    }

    .heroImage {
        margin: 1rem !important;
        position: initial;
    }

    .hero {
        height: 450px !important;
        margin: 0 !important;
    }
}
.spotlight {
    z-index: 9997;
}
.spotlight::before, .spotlight::after {
    content: "";
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    inset: 0px;
    border-radius: inherit;
    background: radial-gradient(750px circle at var(--x) var(--y),rgba(255,255,255,1),transparent 40%);
    z-index: 9998;
}

.spotlight::before {
    z-index: 1;
}

.spotlight::after {
    opacity: 0;
    z-index: 2;
    transition: opacity 350ms ease 0s;
}

.spotlight:hover::after {
    opacity: 1;
}
</style>