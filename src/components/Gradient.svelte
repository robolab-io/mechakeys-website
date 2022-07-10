<div class="hero">
    <div class="gradient">
        <div class="gradientBackground">
            <div class="heroImage" style="">
                <img alt="The MechaKeys application running on Windows" class="app-photo" src="../images/appoverlay.png" style="filter: hue-rotate(0deg) !important; animation: none !important; width: 100%;"/>
            </div>
        </div>
    </div>
</div>

<style>
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
    animation: 900ms linear 0s 1 normal backwards running blur-in;
    display: flex;
    flex-shrink: 1;
    transition: 150ms ease;
}

.heroImage:hover {
    transform: scale(1.05);
    transition: 150ms ease;
}

.hero {

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