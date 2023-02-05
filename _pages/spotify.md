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

#### **Log In with Spotify**

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