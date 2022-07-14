<script>
    import Gradient from '../components/Gradient.svelte'
    import Breathe from '../components/Breathe.svelte'
    import Downloads from '../components/Downloads.svelte'
    import Advertising from '../components/Advertising.svelte'
</script>

<div class="app" style="background-color: #1F1E23; text-rendering: optimizeLegibility; overflow: hidden;">
    <div class="navbar">
        <a href="/" class="logo">
            <svg width="36" height="36" viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M0 13.8062V31L18 13.6489L9.13613 5L0 13.8062Z" fill="#F0F3F8"/>
                <path d="M11 22.3908L19.0021 30L27.7897 22.1429L36 30V13.6667L27.8893 6L11 22.3908Z" fill="#F0F3F8"/>
            </svg>
        </a>

        <div class="links">
            <a href="https://discord.robolab.io" class="navbarLink _1" target="_blank" rel="noopener noreferrer">Discord</a><a href="https://twitter.com/MechaKeys" class="navbarLink _2" target="_blank" rel="noopener noreferrer">Twitter</a><a href="https://mechakeys.reddit.com" class="navbarLink _3" target="_blank" rel="noopener noreferrer">Reddit</a><a href="/terms" class="navbarLink _4">Terms</a><a href="/privacy" class="navbarLink navbarLinkActive _5">Privacy</a>
        </div>
    </div>
    <div class="layout">
        <div class="half">
            <!-- <Breathe/> -->
            <slot></slot>
            <!-- <Breathe/> -->
        </div>
        <Gradient/>
        <img class="glow" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAwAAAAMCAYAAABWdVznAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAGESURBVHgBnVBLbhRBDLVd7prOdIZJK6AoKFLCAoE4DLtcgg1XmKPlFKxZICQUAoj0THdV+YNngZR1Sirbku33nh/Ac567Y0Q85t3Oabfb0bF++v/P4u2t5/vhK70ab3D4Df6Qv9NlNGqttvlx42/ef6Or7ZV+ubuzD5/uHT9+ni6wUbZpQXBKGwaEAmA22zn1vvr5YL3O9VqL5j9J+GD4ujNYZ6ATcuS2JKBW8aQm91aNG+tah9b2Vs6nx4mT4dtu9rNonGKTvjNNIOhJQm9pgOoCS6mgPlWWR4am71KDC1x82zUYSIzJHMmQ4LirquI8q8+TKv1iT3TtrpckPlKFUxLskjm7hW8aO5pMgKp52iPiX7YeXnpOI7KOUHxAhxUqMFgMB5NB8EFqkbdEMPKyoT4Vy9iQAz0FMKIHVliGUcYNdNTGqLlzWfHhjCwwgpUKENDqYMoFQjxQFiOuitnCNS+0lkq8jOkAhFmymvS4yOTdag6CvVO/CHXQ0iCFX8BMg83wDzja7/E7G9ekAAAAAElFTkSuQmCC">
    </div>
    <Advertising/>
</div>

<style>
.glow {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 100vh;
    opacity: .2;
    pointer-events: none;
    z-index: 0;
    filter: blur(0rem);
    animation: 1550ms ease 0s 1 normal running glow-in;
}

@keyframes glow-in {
    0% {
        opacity:0;
        filter: blur(20rem);
    }
    70% {
        opacity:0.7;
        filter: blur(6rem);
    }
    100% {
        opacity:0.2;
        filter: blur(0rem);
    }
}
.logo {
    width: 2.25rem;
    height: 2.25rem;

    display: flex;
    align-self: center;

    animation-name: fade-in-better-logo;
    animation-duration: 1200ms;
    animation-timing-function: ease;
    animation-iteration-count: 1;
    animation-direction: normal;
    animation-fill-mode: backwards;
    animation-play-state: running;
}

.links {
    display: flex;
    align-self: center;
}
.navbarLink {
    font-size: 14px;
    font-family: 'MechaKeys Black';
    color: #F0F3F8;
    transition: 0.2s;
    padding: 1rem;

    animation-name: fade-in-up-better-links;
    animation-duration: 600ms;
    animation-timing-function: ease;
    animation-iteration-count: 1;
    animation-direction: normal;
    animation-fill-mode: backwards;
    animation-play-state: running;
}

.navbarLink._5 {
    animation-delay: 50ms;
}

.navbarLink._4 {
    animation-delay: 100ms;
}

.navbarLink._3 {
    animation-delay: 150ms;
}

.navbarLink._2 {
    animation-delay: 200ms;
}

.navbarLink._1 {
    animation-delay: 250ms;
}

.navbarLink:hover {
    color: #cccfd3;
    transition: 0.2s;
}

.navbar {
    position: absolute;
    top: 0;
    display: flex;
    flex-direction: row;
    padding-top: 1.25rem;
    padding-bottom: 1.25rem;
    padding-left: 2rem;
    padding-right: 2rem;
    flex-shrink: 0;
    /* margin-bottom: 2rem; */
    justify-content: space-between;
    width: 100%;
    z-index: 9998;
    
}

.half {
    height:fit-content;
    display: flex;
    flex-direction: column;
    justify-content: center;

    align-items: center;
    overflow-y: auto;
    overflow-x: hidden;

    flex: 1.25;
}

* { min-width: 0; min-height: 0; }

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  position: relative;
  font-weight: normal;
}

a {
    text-decoration: none;
}

a {
    color: #82a9ec;
}

.layout {
    position: relative;
    overflow: hidden;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: row;
    padding-top: 2rem;
    padding-bottom: 2rem;
}

@keyframes fade-in-up-better-links {
 from {
  opacity:0;
  -webkit-transform:translateY(6px);
  -ms-transform:translateY(6px);
  transform:translateY(6px);
 }
 to {
  opacity:1;
  -webkit-transform:none;
  -ms-transform:none;
  transform:none;
 }
}

@keyframes fade-in-better-logo {
 from {
  opacity:0;
 }
 to {
  opacity:1;
 }
}

@media only screen and (max-width: 800px) {
    .layout {
        flex-direction: column;
        padding-top: 0rem;
        padding-bottom: 0rem;
    }

    .half {
        width: 100%;
        flex: 0
    }

    .links {
        justify-content: flex-end;
    }

    .glow {
        height: 200%;
    }

    .navbar {
        padding-left: 1.5rem !important;
        padding-right: 1.5rem !important;
    }

    .logo {
        flex-shrink: 1;
    }
}
</style>