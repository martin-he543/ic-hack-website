---
layout: page
permalink: /spotify_search.html/
title: Search Results
description: Results to your search.
nav: false
nav_order: 3
---

<script>
    var url = $(location).attr('href');
    var pathname = $(location).attr('pathname');
    songname = url.replace("http://127.0.0.1:4000/ic-hackathon/spotify_search.html/?query=","")
    $("h1").text("Search Results to: " + songname);
</script>

<h1></h1>
<script type="text/javascript" src="assets/js/search.js"></script>
<br />



------------------------------------------
<h5 id="search-result-1" class=".search-result"><b>Song 1</b></h5>
<br />
<iframe style="border-radius:12px" src="https://open.spotify.com/embed/track/4cOdK2wGLETKBW3PvgPWqT?utm_source=generator" width="50%" height="200" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>
------------------------------------------
<h5 id="search-result-2" class=".search-result"><b>Song 2</b></h5>
<br />
<iframe style="border-radius:12px" src="https://open.spotify.com/embed/track/0i8kmubjCbHEuMABXMXCqG?utm_source=generator" width="50%" height="200" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>
------------------------------------------
<h5 id="search-result-3" class=".search-result"><b>Song 3</b></h5>
<br />
<iframe style="border-radius:12px" src="https://open.spotify.com/embed/track/3pepZAOvUCBt3qWi9Ax6Aq?utm_source=generator" width="50%" height="200" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>
------------------------------------------
<h5 id="search-result-4" class=".search-result"><b>Song 4</b></h5>
<br />
<iframe style="border-radius:12px" src="https://open.spotify.com/embed/track/4FFsEzul2cilyNLMctY2sP?utm_source=generator" width="50%" height="200" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>
------------------------------------------
<h5 id="search-result-5" class=".search-result"><b>Song 5</b></h5>
<br />
<iframe style="border-radius:12px" src="https://open.spotify.com/embed/track/0yfIY2OJkrVNeZKCRGw2bo?utm_source=generator" width="50%" height="200" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>
---