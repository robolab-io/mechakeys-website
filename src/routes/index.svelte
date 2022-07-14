<script>
    import Downloads from '../components/Downloads.svelte'
    import Breathe from '../components/Breathe.svelte'
</script>

<div class="ctaContent">
    <div class="heading">The desktop sound simulator</div>
    <div class="description">
        MechaKeys is the most popular keyboard and mouse simulator for desktop. The easiest solution to add immersion to your typing, gaming, streaming, and more.
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
    z-index: 1;
}

.description {
    font-size: 18px;
    font-family: 'MechaKeys Standard';
    line-height: 135%;
    color: #8C939E;
    margin-bottom: 2rem;
    z-index: 1;
}

.ctaContent {
    max-width: 550px;
    /* margin: auto 4rem auto 4rem; */
    margin: auto 4rem auto 4rem;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    z-index: 1;
    height: 700px;
}
</style>