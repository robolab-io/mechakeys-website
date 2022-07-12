<script>
    import Gradient from '../components/Gradient.svelte'
    import Breathe from '../components/Breathe.svelte'
    import Downloads from '../components/Downloads.svelte'
</script>

<div class="app" style="background-color: #1F1E23; text-rendering: optimizeLegibility; overflow: hidden;">
    <div class="layout">
        <div class="half">
            <div class="navbar">
                <a href="/" class="logo">
                    <svg width="36" height="36" viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0 13.8062V31L18 13.6489L9.13613 5L0 13.8062Z" fill="#F0F3F8"/>
                        <path d="M11 22.3908L19.0021 30L27.7897 22.1429L36 30V13.6667L27.8893 6L11 22.3908Z" fill="#F0F3F8"/>
                    </svg>
                </a>
    
                <div class="links">
                    <a href="https://discord.robolab.io" class="navbarLink" target="_blank" rel="noopener noreferrer">Discord</a><a href="/terms" class="navbarLink">Terms</a><a href="/privacy" class="navbarLink navbarLinkActive">Privacy</a>
                </div>
            </div>
            <Breathe/>
            <slot></slot>
            <Breathe/>
        </div>
        <Gradient/>
    </div>
    <div class="section sectiondark">
        <div class="sectionContent">
            <div class="sectionImage"><img class="image" src="../images/rocket-hero.png" alt=""/></div>
            <div class="gradients" style="--color-a: #BA2DB7; --color-b: #CF3C7E; --color-c: #E94F35;"></div>
            <div class="sectionText">
                <div class="sectionTitle">Maximum performance</div>
                <div class="sectionDescription">MechaKeys is built for native speeds on any device. Experience the lowest latency possible from a sound simulator. An optimized frontend and a custom-built input detector create a realistic typing experience.</div>
            </div>
        </div>
    </div>
    <div class="section">
        <div class="sectionContent">
            <div class="sectionText">
                <div class="sectionTitle">Truly customizable</div>
                <div class="sectionDescription">A huge variety of different keyboard switches from your favorite manufacturers are already in MechaKeys. Everything is an option - customize MechaKeys in a way that works for you.</div>
            </div>
            <div class="sectionImage"><img class="image" src="../images/switch-hero.png" alt=""/></div>
            <div class="gradients gradientsRight" style="--color-a: #7a2dba; --color-b: #523ccf; --color-c: #35cee9;"></div>
        </div>
    </div>
    <div class="section sectiondark">
        <div class="sectionContent">
            <div class="sectionImage"><img class="image" src="../images/community-hero.png" alt=""/></div>
            <div class="gradients" style="--color-a: #BA2DB7; --color-b: #CF3C7E; --color-c: #E94F35;"></div>
            <div class="sectionText">
                <div class="sectionTitle">Community powered</div>
                <div class="sectionDescription">Our Discord community provides direct access to in-app rewards and contact with the developers to share feedback and requests. Soon, a community store will be available to share your creations!</div>
            </div>
        </div>
    </div>
    <div class="section">
        <div class="endingSectionContent">
            <div class="endingSectionText">
                <div class="sectionTitle">Download the best keyboard simulator.</div>
                <div class="sectionDescription">MechaKeys is free, forever, for personal use.</div>
            </div>
        </div>
        <Downloads/>
        <Breathe/>
    </div>
</div>

<style>
.gradients {
    pointer-events: none;
    user-select: none;
    position: absolute;
    overflow: visible;
    z-index: 3001;
    inset: 0px;
}

.gradients:before {
    content: "";
    position: absolute;
    opacity: 0.2;
    top: 50%;
    left: 35%;
    transform: translate(-50%, -50%);
    width: calc(-50px + 100vw);
    height: 20vh;
    filter: blur(80px); 
    background: radial-gradient(400px circle at 40% 45%, var(--color-a), 70%, transparent ), radial-gradient(400px circle at 50% 55%,var(--color-b),60%,transparent), radial-gradient(350px circle at 40% 40%,var(--color-c),60%,transparent);
}

.gradientsRight:before {
    content: "";
    position: absolute;
    opacity: 0.2;
    top: 50%;
    left: 75%;
    transform: translate(-50%, -50%);
    width: calc(-50px + 100vw);
    height: 20vh;
    filter: blur(80px); 
    background: radial-gradient(400px circle at 40% 45%, var(--color-a), 70%, transparent ), radial-gradient(400px circle at 50% 55%,var(--color-b),60%,transparent), radial-gradient(350px circle at 40% 40%,var(--color-c),60%,transparent);
}
.sectionDescription {
    word-wrap: break-word;
    color: #8C939E;
    font-size: 18px;
    font-family: 'MechaKeys Standard';
    animation-name: fade-in-up-better;
    animation-duration: 800ms;
    animation-timing-function: ease;
    animation-iteration-count: 1;
    animation-direction: normal;
    animation-fill-mode: backwards;
    animation-play-state: running;
}
.sectionTitle {
    font-size: clamp(20px,3vw,40px);
    font-family: 'MechaKeys Black';
    animation-name: fade-in-up-better;
    animation-duration: 800ms;
    animation-timing-function: ease;
    animation-iteration-count: 1;
    animation-direction: normal;
    animation-fill-mode: backwards;
    animation-play-state: running;
}
.image {
    width: 100%;
    object-fit: cover;
}
.sectionImage {
    max-width: 550px;
    max-height: 350px;
    animation-name: fade-in-up-better;
    animation-duration: 800ms;
    animation-timing-function: ease;
    animation-iteration-count: 1;
    animation-direction: normal;
    animation-fill-mode: backwards;
    animation-play-state: running;
    animation-delay: calc(var(--base-delay) + 150ms); 
}

.sectionText {
    display: flex;
    flex-direction: column;
    justify-content: center;
    max-width: 500px;
}

.section {
    width: 100%;
    display: flex;
    align-items: center;
    flex-direction: column;
}

.section.sectiondark {
    background-color: #151418;
}

.sectionContent {
    width: 100%;
    max-width: 1260px;
    box-sizing: border-box;
    display: flex;
    flex-direction: row;
    padding: 4rem;
    align-items: center;
}

.endingSectionContent {
    display: flex;
    flex-direction: row;
    padding: 4rem;
    align-items: center;
}
.logo {
    width: 2.5rem;
    height: 2.5rem;
}

.links {
    align-self: center;
}
.navbarLink {
    font-size: 18px;
    font-family: 'MechaKeys Black';
    color: #F0F3F8;
    transition: 0.2s;
    padding: 1rem;
}

.navbarLink:hover {
    color: #cccfd3;
    transition: 0.2s;
}

.navbar {
    position: sticky;
    top: 0;
    display: flex;
    flex-direction: row;
    padding-top: 1.25rem;
    padding-bottom: 1.25rem;
    padding-left: 2rem;
    padding-right: 2rem;
    flex-shrink: 0;
    margin-bottom: 2rem;
    justify-content: space-between;
    width: 100%;
    background-color: #0e0c11;
    z-index: 9998;
}

.half {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;

    align-items: center;
    overflow-y: auto;
    overflow-x: hidden;

    flex: 1;
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
}

@keyframes fade-in-up-better {
 from {
  opacity:0;
  -webkit-transform:translateY(20px);
  -ms-transform:translateY(20px);
  transform:translateY(20px);
 }
 to {
  opacity:1;
  -webkit-transform:none;
  -ms-transform:none;
  transform:none;
 }
}

@media only screen and (max-width: 800px) {
    .layout {
        flex-direction: column;
    }

    .half {
        width: 100%;
        flex: 0
    }

    .links {
        justify-content: flex-end;
    }

    .sectionContent {
        padding: 2rem !important;
        flex-direction: column;
    }
    
    .sectionImage {
        max-width: 400px;
        max-height: 260px;
    }
}
</style>