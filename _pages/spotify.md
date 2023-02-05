---
layout: page
permalink: /spotify/
title: Spotify
description: Connect with your Spotify account.
nav: true
nav_order: 1
---

*Role : Administrator*

<!-- <script>
  $('#search-ui').submit(function() {
      // Get all the forms elements and their values in one step
      var values = $(this).serialize();
      $( "#results" ).text( str );
  });
</script> -->


  <form action="{{ site.baseurl }}/spotify_search.html" method="get" id="search-ui">
    <!-- <label for="search-box">Search: </label> -->
    <h5><i class="fab fa-spotify"></i><b> Log In with Spotify</b></h5>
    <i class="fas fa-user"></i> <input type="text" class="search-box" name="query" placeholder="🎶 Spotify Username" target="">
    <br />
    <i class="fas fa-unlock"></i> <input type="password" class="search-box" name="query" placeholder="🎶 Spotify Password"  target="">
    <br /><br /><br />
    <i class="fas fa-search"></i> <input type="number" class="search-box" name="query" placeholder="🔎 Search Song..." target="">
    <button type="submit">
      <i class="fab fa-spotify"></i>
    </button>
    <!-- <input type="submit" value="🔍" id="search-button"> -->
  </form>
<br />

##### **Playlist Name**



*Role : Participant*

###### **Add a Song:** 
<form action="{{ site.baseurl }}/spotify_search.html" method="get" id="search-ui">
  <input type="text" class="search-box" name="query" placeholder="Search Song">
  <button type="submit">
    <i class="fas fa-search"></i>
  </button>
</form>


---