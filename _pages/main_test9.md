---

type: page
permalink: /main_test9
layout: splash
classes: landing


---


<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
.background {
    background: url("/new-theme/assets/images/dukehumphreys.jpg");
    position: relative;
    width: 100%;
    height: 100%;
}

.layer {
    background-color: rgba(248, 247, 216, 0.7);
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}

.centered {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
</style>
</head>
<body>

<h2>Radial Gradient as Background Image</h2>
<p>This radial gradient starts in the center. It starts red, transitioning to yellow:</p>

<div class="background">
    <div class="layer"></div>
    <div class="centered">Reproducible Research Oxford is a project based at the University of
    Oxford. We are the local branch of the UK Reproducibility Network and
    aim to lay the groundwork for a culture of reproducibility and open
    research practices in Oxford. To that purpose, we organise events, and
    have set up a network of ambassadors who provide information and
    initiate conversation on these issues at their departments.</div>
</div>

</body>
</html>
