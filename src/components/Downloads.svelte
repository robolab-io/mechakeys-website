<script>

</script>

<div class="downloadButtonWrapper">
    <a href="" class="downloadButton">Download for Windows</a>
    <a href="" class="downloadLink">Other platforms</a>
</div>

<style>
.downloadButtonWrapper {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    white-space: nowrap;
    gap: 1rem;
}

.downloadButton {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 12px 40px;
    font-weight: 500;
    background: #0e0c11;
    background-clip: border-box;
    background-clip: padding-box;
    border: 1px solid transparent;
    color: #F0F3F8 !important;
    border-radius: 8px;
    box-shadow: 0px 0px 32px rgba(52, 50, 137, 0.6);
    transition: 0.2s;
    white-space: nowrap;
    position: relative
}

.downloadButton {
    text-decoration: none;
}

.downloadLink {
    font-family: 'MechaKeys Black';
    font-size: 18px;
}

.downloadLink {
    color: #82a9ec;
    transition: 0.2s;
}

.downloadLink {
    text-decoration: none;
}

.downloadLink:hover {
    color: #b1caf5;
    transition: 0.2s;
}

.downloadButton {
    font-family: 'MechaKeys Black';
    font-size: 18px;
}

.downloadButton:hover {
    box-shadow: 0px 0px 70px rgba(50, 66, 137, 0.9);
    background-color: #1d1924;
    transition: 0.2s;
}

.downloadButton::before {
    content: "";
    position: absolute;
    inset: 0;
    z-index: -1;
    opacity: .8;
    margin: -3px;
    border-radius: inherit;
    transition: opacity .2s;
    background: linear-gradient(135deg,#ff2136,#9b4dff 50%,#0294fe);
}

.downloadButton:hover::before {
    background: linear-gradient(135deg,#ff21aa,#4db8ff 50%,#02fec7);
    transition: opacity .2s;
    opacity: 1;
}
</style>