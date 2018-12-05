---

type: page
permalink: /main_test10
layout: splash
classes: landing


---


<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
.container {
      position: relative;
      width: 600px;
      height: 400px;
    }

    .someimg {
        postion: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
      }

    .overlay {
        position: absolute;
        top: 0;
        left: 0;
        clear: float;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.6);
        color: #ffffff;
      }
</style>
</head>

  <body>

    <div id="container">
      <img id="someimg" src="assets/images/dukehumphreys.jpg" alt="image">
      <div id="overlay">This is some text in an overlay</div>
    </div>

  </body>
</html>
