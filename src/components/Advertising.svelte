<script>
    import Breathe from '../components/Breathe.svelte'
    import Downloads from '../components/Downloads.svelte'
</script>

<div class="sections">
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
                <div class="sectionTitle">Download MechaKeys</div>
                <div class="sectionDescription">Free to download, free to use, available for every device. Join over 600,000 other people!</div>
            </div>
            <div class="endingDownloads">
                <Downloads/>
                <Breathe/>
            </div>
        </div>
    </div>
    <div class="section">
        <div class="copyright">© 2022 Robolab LLC. All rights reserved.</div>
        <img style="position: absolute; top: 0; left: 0; z-index: -1; width: 100%; opacity: .2; pointer-events: none;" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAwAAAAMCAYAAABWdVznAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAGOSURBVHgBvVFLbhNBEH1V3T2emdg4AfxJFO9AoMkKxAFYI3Ens+YEnIMDsEKsWIDIbIgQigSWg+wIz3i+1d00YkMukFq9V6pXVa+K3rx8mw6UOo5EZd65pyB+WCTR8Nf9dH85H3/7OR1/Xs2HX7Ykq++fDkuNODYd9Ahwp6qRx8rSI80YcYOGOgzZ+XogcoWJuc4yVHprYo6I4oh5zK27y8RHda9HVZt0Ukd7bnnetxhzqaJqAta0SFyxIdhCgZRRYrXuxKimZG2v44SMSZXSJhoiDAX0x9msm63LPUlcoQ+1jfbOKvY9MwnMoGd15EPnBO59D6fx4dTWd1Y77v0Vi157RwsvKqjg2VEdwTcHrm8aBEcvguDsDHJ+botY4gtj6R6YOjaYeGIVDrEN7Oug4PVBLu3yNRwBnrIsN8+OF6Owwwm1/kQRDsWSUoYqR3bVS3L5YJNuljl1GiCf5+im03e/n1w8r3aL3Y/wk8hJzZ2NJZn6tlynNfJXEjyDcCP8X07L/zIB+3+IPG4l/gCInrnOZomQAAAAAABJRU5ErkJggg==" alt="">
    </div>
</div>

<style>
    * {
        --base-delay: 1500ms
    }
.copyright {
    color: #8C939E;
    font-size: 12px;
    font-family: 'MechaKeys Standard';
    padding: 2rem;
}
.endingDownloads {
    margin-top: 2rem;
    align-self: flex-start;
    display: flex;
    flex-direction: column;
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
    animation-delay: calc(var(--base-delay) + 350ms);
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
    animation-delay: calc(var(--base-delay)  + 300ms);
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
    animation-delay: calc(var(--base-delay) + 0ms);
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
    flex-direction: column;
    padding: 4rem 4rem 0 4rem;
    align-items: center;
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