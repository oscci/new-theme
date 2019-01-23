---

type: page
permalink: /
layout: splash
classes: landing

---

<style>
body {
  background-image: url({{ 'assets/images/radcliffe_camera.jpg' | relative_url }});
  background-attachment: fixed;
  background-size: cover;
  background-position-y: center;
  margin-bottom: 0 !important;
}
.initial-content {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.container {
  color: #fff;
  background-color: #00193b;
  padding: 1em;
  text-align: justify;
}
</style>

<div class="container">
  <p>Reproducible Research Oxford is a project based at the <a href="https://www.ox.ac.uk/">University of
  Oxford</a>. We are the local branch of the <a href="http://ukrn.org/">UK Reproducibility Network</a> and
  aim to lay the groundwork for a culture of reproducibility and open
  research practices in Oxford.</p>
  <p>To that purpose, we organise <a href="{{ '/initiatives' | relative_url }}">initiatives</a>, and
  have set up a network of <a href="{{ '/people' | relative_url }}">ambassadors</a> who provide information and initiate conversation on these issues at their departments. We also maintain a list of helpful <a href="{{ '/resources' | relative_url }}">resources</a>.</p>
  <p>If you're affiliated with Oxford and are interested in reproducible research, <a href="{{ '/get-involved' | relative_url }}">join us</a>!</p>
</div>
