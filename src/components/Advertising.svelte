<script>
    import Breathe from '../components/Breathe.svelte'
    import Downloads from '../components/Downloads.svelte'
</script>
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
        <div class="endingDownloads">
            <Downloads/>
            <Breathe/>
        </div>
    </div>
</div>
<div class="section">
    <div class="copyright">Copyright (c) 2022 Robolab, Fero</div>
</div>

<style>
.copyright {
    color: #8C939E;
    font-size: 12px;
    font-family: 'MechaKeys Standard';
    padding: 1rem;
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
    animation-delay: 350ms;
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
    animation-delay: 300ms;
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