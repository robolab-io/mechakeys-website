<script>
    import Downloads from '../components/Downloads.svelte'
    import Breathe from '../components/Breathe.svelte'
</script>

<div class="ctaContent">
    <div class="heading">MechaKeys is a desktop customization tool.</div>
    <div class="description">
        The most popular keyboard and mouse simulator. MechaKeys is the integrated typing environment built for blazing-fast performance, a modern interface, and open development.
    </div>
    <Downloads/>

    <Breathe/>
</div>

<style>
.heading {
    font-size: clamp(28px,3vw,46px);
    font-family: 'MechaKeys Black';
    line-height: 135%;
    color: #F0F3F8;
    margin-bottom: 2rem;
}

.description {
    font-size: 18px;
    font-family: 'MechaKeys Standard';
    line-height: 135%;
    color: #8C939E;
    margin-bottom: 2rem;
}

.ctaContent {
    max-width: 550px;
    /* margin: auto 4rem auto 4rem; */
    margin: auto 4rem auto 4rem;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}
</style>