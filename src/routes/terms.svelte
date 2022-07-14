<script>
    import Breathe from '../components/Breathe.svelte'
</script>

<div class="tosContent">
    <div class="gobackhome"><a href="/">← Go back home</a></div>
    <div class="heading">Terms of Service</div>
    <div class="description">
        Please read our <a href="/privacy">Privacy Policy</a>.
    </div>
    <div class="description">
        You must be a minimum of 13 years of age to use our services.
    </div>
    <div class="description">
        Accounts are entirely the responsibility of the user. Thus any activity performed by that account will be attributed to the owner of the account, regardless of whether or not the activity was performaed by you, or any other individual or entity that may be using the account. Robolab is not responsible nor liable for any activity that happens on user accounts.
    </div>
    <div class="description">
        You agree that the information used to create your account on our services is accurate, current, and complete. 
    </div>
    <div class="description">
        Robolab is not to be held responsible or liable for any damages caused or incurred, directly or indirectly, from the usage or access of our services. You agree to hold Robolab harmless from and against any liabilities, damages, costs, and expenses.
    </div>
    <div class="description">
        Robolab grants permission to use, access, and download our services we provide on our websites for personal, non-commercial use only. You agree to use Robolab services under a limited, irrevocable, non-transferable license. You agree that while you use and access our services, and while the agreement to these Terms are in effect, you cannot, will not attempt to, or assist anyone to
        <ul>
            <li>Copy, modify, adapt, distribute, sell, transfer, license, transmit, stream, publicly display, publicly use, or abuse source code from any of our services</li>
            <li>Use any services in a way not outlined in these Terms</li>
            <li>Use any services for monetary gain, for the purposes of, or to contribute to, directly or indirectly</li>
            <li>Reverse engineer, decompile, exploit, damage, or otherwise modify any of our services</li>
            <li>Hack, phish, exploit, or cheat in any of our services</li>
            <li>Use any services in an illegal manner</li>
            <li>Steal, pirate, torrent, or otherwise download any services, or any dependencies, or any resources, or any files, or any references in any of our services in any manner other than Robolab websites.</li>
            <li>Modify files in any of our services while they are downloaded, including the deletion, addition, or copying of.</li>
        </ul>
    </div>
    <div class="description">
        No licenses, grants, or rights are given to you, by implication, or otherwise under any intellectual property rights owned or controlled by Robolab. You may not use "MechaKeys" or "Robolab" and their respective logomarks as your own.             
    </div>
    <div class="description">
        Robolab reserves the right, at any point in time, to reject any email, username, data, or information that you provide to our services. Robolab reserves the right to refuse and revoke access to usage or access of our services, without notice, for any reason, at any time, and for any length of time. Robolab is under no obligation to compensate you for any loss, including any lost premium products purchased on our services. Robolab does not provide refunds for any premium products purchased on our services, except at our sole discretion. You agree that when purchasing a premium product, that the purchase you performed is final, non-refundable, non-exchangable, and non-transferable, except at our sole discretion. Robolab reserves the right to reverse and prevent future purchases from your account.
    </div>
    <div class="description">
        If a user is using our services on behalf of or acting as a business or legal entity, and not in an indiviudal capacity, you will indemnify and hold Robolab and its officers, directors, employees, and agents harmless from and against any claims, liabilities, damages, and costs related to your access or use of our services or your violation of these Terms of Service.                        
    </div>
    <div class="description">
        All users of our services may contact Robolab for any inquiries via e-mail. Please contact mail (dot) robolab (dot) io (at) gmail.com                    
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
    
    .tosContent {
        max-width: 550px;
        /* margin: auto 4rem auto 4rem; */
        margin: auto 4rem auto 4rem;
        margin-top: 6rem;
        height: 100%;
    }
    </style>