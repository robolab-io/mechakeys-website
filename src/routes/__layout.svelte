<script>
    import Gradient from '../components/Gradient.svelte'
    import Breathe from '../components/Breathe.svelte'
    import Downloads from '../components/Downloads.svelte'
    import Advertising from '../components/Advertising.svelte'
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
                    <a href="https://discord.robolab.io" class="navbarLink _1" target="_blank" rel="noopener noreferrer">Discord</a><a href="/terms" class="navbarLink _2">Terms</a><a href="/privacy" class="navbarLink navbarLinkActive _3">Privacy</a>
                </div>
            </div>
            <Breathe/>
            <slot></slot>
            <Breathe/>
        </div>
        <Gradient/>
    </div>
    <Advertising/>
</div>

<style>
.logo {
    width: 2.5rem;
    height: 2.5rem;
}

.links {
    align-self: center;
}
.navbarLink {
    font-size: 14px;
    font-family: 'MechaKeys Black';
    color: #F0F3F8;
    transition: 0.2s;
    padding: 1rem;

    animation-name: fade-in-up-better-links;
    animation-duration: 1200ms;
    animation-timing-function: ease;
    animation-iteration-count: 1;
    animation-direction: normal;
    animation-fill-mode: backwards;
    animation-play-state: running;
}

.navbarLink._1 {
    animation-delay: 50ms;
}

.navbarLink._2 {
    animation-delay: 100ms;
}

.navbarLink._3 {
    animation-delay: 150ms;
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

@keyframes fade-in-up-better-links {
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
}
</style>