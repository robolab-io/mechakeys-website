<script>
    import { onMount } from 'svelte'

    onMount(() => {
        // Thanks to Ryan Finni
        // https://letsbuildui.dev/articles/a-3d-hover-effect-using-css-transforms

        const card = document.querySelector(".heroImage");
        const photo = document.querySelector(".appphoto");

        const bg = document.querySelector(".gradientBackground");
        const THRESHOLD = 2;

        function handleHover(e) {
            const { clientX, clientY, currentTarget } = e;
            const { clientWidth, clientHeight, offsetLeft, offsetTop } = currentTarget;
            const horizontal = (clientX - offsetLeft) / clientWidth;
            const vertical = (clientY - offsetTop) / clientHeight;
            const rotateX = (THRESHOLD / 2 - horizontal * THRESHOLD).toFixed(2);
            const rotateY = (vertical * THRESHOLD - THRESHOLD / 2).toFixed(2);
            const reflectPower = vertical > 0.5 ? vertical - 0.5 : 0;
            const reflectLeft = horizontal * 100;
            const reflectTop = vertical * 100;
            
            card.style.transform =
                `perspective(${clientWidth}px) rotateX(${rotateY}deg) rotateY(${rotateX}deg) scale3d(1, 1, 1)`;
            card.style.setProperty("--x", clientX)
            card.style.setProperty("--y", clientY)
            card.style.setProperty("--realWidth", clientWidth)
            card.style.setProperty("--h", horizontal)
            card.style.setProperty("--v", vertical)
            card.style.setProperty("--reflect-power", reflectPower);
            card.style.setProperty("--reflect-left", `${reflectLeft}%`);
            card.style.setProperty("--reflect-top", `${reflectTop}%`);

            photo.style.setProperty("--x", clientX)
            photo.style.setProperty("--y", clientY)
            photo.style.setProperty("--realWidth", clientWidth)
            photo.style.setProperty("--h", horizontal)
            photo.style.setProperty("--v", vertical)
            photo.style.setProperty("--reflect-power", reflectPower);
            photo.style.setProperty("--reflect-left", `${reflectLeft}%`);
            photo.style.setProperty("--reflect-top", `${reflectTop}%`);

            bg.style.setProperty("--total-power", reflectPower + 5);
            
        }

        function resetStyles(e) {
            card.style.transform =
                `perspective(${e.currentTarget.clientWidth}px) rotateX(0deg) rotateY(0deg)`;
            
            card.style.setProperty("--reflect-power", 0);
        }

        card.addEventListener("mousemove", handleHover);
        card.addEventListener("mouseleave", resetStyles);
    })
</script>
<div class="hero">
    <div class="gradient">
        <div class="gradientBackground">
            <div class="heroImage" style="">
                <video alt="The MechaKeys application running on Windows" class="appphoto" src="../images/appvideo.mp4" autoplay="true" muted="true" loop="true" style="filter: hue-rotate(0deg) !important; animation: none !important;"></video>
            </div>
        </div>
    </div>
</div>

<style lang="scss">
.appphoto {
    border-radius: 1rem;
    width: 100%;
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
    width: 750px;
    border-radius: 0.75rem;

    position: relative;
    transition: 600ms;
    transform-style: preserve-3d;
    will-change: transform;

    opacity: 0.89;
    margin: 1rem;
}

.heroImage:before {
    content: "";
    position: absolute;
    height: 100%;
    width: 100%;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    z-index: 0;
}
			
.heroImage:after {
    content: "";
        background:  radial-gradient(rgba(255, 255, 255, 0.2), rgba(255, 255, 255, 0));
        position: absolute;
        padding-top: 220%;
        width: 600%;
        z-index: 2;
        top: var(--reflect-top, 0);
        left: var(--reflect-left, 0);
        opacity: var(--reflect-power, 0);
        transition: opacity .3s ease;
}

.heroImage:hover{
    transition-duration: .1s;
    opacity: 1;
}

.heroImage:hover > .heroImage:after {
    transition-duration: .1s;
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
</style>