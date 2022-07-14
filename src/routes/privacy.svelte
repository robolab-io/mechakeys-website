<script>
    import Breathe from '../components/Breathe.svelte'
</script>

<div class="privacyContent">
    <div class="gobackhome"><a href="/">← Go back home</a></div>
    <div class="heading">Privacy Policy</div>

    <div class="description">
        Please read our <a href="/terms">Terms of Service</a>.
    </div>
    <div class="description">
        We do not sell your personal information. That's our policy in one sentence. No information provided or automatically collected will be sold or transferred outside of Robolab. Your information is only used for the purposes of our services and their security. We only store information for as long as you use our services.
    </div>
    <div class="description">
        When you create an account and access our services using that account, you provide Robolab with an email and username for identification purposes only.
    </div>
    <div class="description">
        When you perform actions on our services, which includes, but is not limited to, purchasing digital items on our services, checking your account's achievements, or viewing a leaderboard, Robolab will automatically receive information such as your IP address, and may store attributes and related metadata about that request, such as whether it was successful and how it was accessed. 
    </div>
    <div class="description">
        In the event where the Terms of Service is breached, Robolab may store your IP address for security and authenticity purposes only.    
    </div>
    <div class="description">
        Robolab does not use cookies, third-party analytics, advertising systems, or similar tracking technologies on our websites and services.
    </div>
    <div class="description">
        When paying for premium products on our services, Robolab does not receive nor store your payment information. This information is entirely handled by Stripe or PayPal, and their respective privacy policies apply.
    </div>
    <div class="description">
        Data and information is processed in the United States. All users of our services have the same rights regarding their data regardless of geographic location. The legal entity responsible for such processing is Robolab LLC.
    </div>
    <div class="description">
        All users of our services may request a copy of their data, and request that their data be removed from our services via e-mail. Please contact mail (dot) robolab (dot) io (at) gmail.com
    </div>
</div>

<style>
    a {
        text-decoration: none;
    }

    a {
        color: #82a9ec;
        transition: 0.2s;
    }

    a:hover {
        color: #b1caf5;
        transition: 0.2s;
    }
    
    .gobackhome {
        font-family: 'MechaKeys Standard';
        margin-bottom: 2rem;
    }

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
    
    .privacyContent {
        max-width: 550px;
        /* margin: auto 4rem auto 4rem; */
        margin: auto 4rem auto 4rem;
        height: 100%;
        margin-top: 6rem;
    }
    </style>