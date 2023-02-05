---
layout: page
title: Carpool
permalink: /carpool/
subtitle: Use our carpooling optimisation to minimise your parties carbon emissions!
nav: true
profile:
  align: right
  image: demonic.jpg
  image_circular: true # crops the image to make it circularS
  address: >
     <p style="text-align:center;"><b>Now Available Worldwide</b></p>
     <p style="text-align:center;">physteem@outlook.com</p>

news: true  # includes a list of news items
selected_papers: true # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page
---
## <a class="wow fadeIn" data-wow-delay="0.5s">Connect to your ride, in moments.</a>
<script src="https://unpkg.com/@googlemaps/markerclusterer/dist/index.min.js"></script>
<script type="text/javascript">
    const markerCluster = new markerClusterer.MarkerClusterer({ map, markers });
</script>
<script src="assets/typescript/index.ts"></script>

<script type="text/javascript">
    // Initialize and add the map
    function initMap() {
    // The location of Uluru
    const locations = [{ lat: -25.344, lng: 131.031 },
    { lat: -30.344, lng: 136.031 },
    { lat: -31.344, lng: 136.031 },
    { lat: -32.344, lng: 136.031 }];
    markers = []

    console.log(locations[0]);
    console.log('---------------------hi------------------------')
    // The map, centered at Uluru
    const map = new google.maps.Map(document.getElementById("map"), {
        zoom: 4,
        center: locations[0],
    });
    // The marker, positioned at Uluru
    // const marker = new google.maps.Marker({
    //     position: locations[0],
    //     map: map,
    // });

    // const marker1 = new google.maps.Marker({
    //     position: locations[1],
    //     map: map
    // });
    const labels = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    for (let i = 0; i <= locations.length; i++) {
        var marker = new google.maps.Marker({
            position: locations[i],
            map: map,
            label: labels[i]
        });
    };
    }

    window.initMap = initMap;

    var post_carpooling = (event_id, account_ids, carpooler_id = null) => {
        var myHeaders = new Headers();
        myHeaders.append("Content-Type", "application/json");
        var raw = JSON.stringify({ "event_id": event_id, "account_ids": account_ids, "carpooler_id": carpooler_id });
        var requestOptions = {
            method: 'POST',
            headers: myHeaders,
            body: raw,
            redirect: 'follow'
        };
        fetch("https://cwfusu2ly0.execute-api.eu-west-2.amazonaws.com/Prod/carpooling", requestOptions)
            .then((response) => {
                if (response.ok) {
                    return response.json();
                } else {
                    throw new Error('Server response wasn\'t OK');
                }
            })
            .then((data) => {
                return data.statusCode;
            });
    }

    const wrapper = document.querySelectorAll('.progress');
    const barCount = 50; // number of bars
    const percentDemo = 50 * 90/100; // 90%
    for (let index = 0; index < barCount; index++) {
    const className = index < percentDemo ? 'selected-demo' : '';
    wrapper[0].innerHTML += `<i style="--i: ${index};" class="${className}"></i>`;
    }
    wrapper[0].innerHTML += `<p class="selected percent-text text-demo">90%</p>`
</script>

<head>
    <script src="https://polyfill.io/v3/polyfill.min.js?features=default"></script>
    <link rel="stylesheet" type="text/css" href="./style.css" />
    <script type="module" src="./index.js"></script>
<script
      type="text/javascript"
      src="https://www.gstatic.com/charts/loader.js"
    ></script>
    <script type="text/javascript">
      google.charts.load("current", { packages: ["gauge"] });
      google.charts.setOnLoadCallback(drawChart);

      function drawChart() {
        var data = google.visualization.arrayToDataTable([
          ["Label", "Value"],
          ["CO2 %", 60]
        ]);

        var options = {
          width: 400,
          height: 120,
          redFrom: 90,
          redTo: 100,
          yellowFrom: 75,
          yellowTo: 90,
          minorTicks: 5
        };

        var chart = new google.visualization.Gauge(
          document.getElementById("chart_div")
        );

        chart.draw(data, options);
      }
    </script>
</head>
  
<style>
    /* Set the size of the div element that contains the map */
    #map {
    height: 400px; /* The height is 400 pixels */
    width: 100%; /* The width is the width of the web page */
    border-radius: 25px;

    .progress {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    }
    .progress i {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    transform: rotate(calc(45deg + calc(calc(360deg / var(--tlt-br-cnt)) * var(--i))));
    }
    .progress i::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    background: hsla(0, 0%,100%, 12%);;
    width: 5px;
    height: 20px;
    border-radius: 999rem;
    transform: rotate(-45deg);
    transform-origin: top;
    opacity: 0;
    animation: barCreationAnimation 100ms ease forwards;
    animation-delay: calc(var(--i) * 15ms);
    }
    .progress .selected-demo::after {
    background: hsl(130, 100%, 50%);
    box-shadow: 0 0 1px hsl(130, 100%, 50%),
                0 0 3px hsl(130, 100%, 30%),
                0 0 4px hsl(130, 100%, 10%);
    }

    .percent-text {
    font-size: 3rem;
    animation: barCreationAnimation 500ms ease forwards;
    animation-delay: calc(var(--tlt-br-cnt) * 15ms / 2);
    }
    .text-demo{
    color: hsl(130, 100%, 50%);
    text-shadow: 0 0 1px hsl(130, 100%, 50%),
                    0 0 3px hsl(130, 100%, 30%),
                    0 0 4px hsl(130, 100%, 10%);
    opacity: 0;
    }
</style>

<body>
    <div class="card mt-3 wow fadeIn" id="participant" data-wow-delay="1s" style="padding: 3rem; overflow-y: scroll; height: 300px;">
    <h2>Participants</h2>
        <fieldset>
            <legend>Choose your fellow riders:</legend>
            <div>
            <input type="checkbox" id="scales" name="scales" checked>
            <label for="scales">Laura</label>
            </div>
            <div>
            <input type="checkbox" id="horns" name="horns">
            <label for="horns">Jonte</label>
            </div>
            <div>
            <input type="checkbox" id="horns" name="horns">
            <label for="horns">Jamie</label>
            <div>
            <input type="checkbox" id="horns" name="horns">
            <label for="horns">Thomas</label>
            <div>
            <input type="checkbox" id="horns" name="horns">
            <label for="horns">Martin</label>
            <div>
            <input type="checkbox" id="horns" name="horns">
            <label for="horns">Denis</label>
            </div>
            </div>
            </div>
            </div>
        </fieldset>
    </div>
    <br />
    <div id="map">
    </div>
    <br />
    <br />



<div class="card mt-3 wow fadeIn" id="participant" data-wow-delay="1s" style="padding: 3rem;">
<h4>Carpool CO₂ Saved:</h4><div id="chart_div" style="width: 120px; height: 120px; "></div>
<br /><br />
<h4>Total Time Taken for Journey: 29 minutes</h4>
</div>

<script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyAloqkgOYYEh1XSRaPB6Yj85cyuQKUfFxg&callback=initMap&v=weekly" defer></script>

</body>
