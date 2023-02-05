---
layout: page
permalink: /login/
title: Log In / Sign Up
description: Log in to an existing account, or create a new account.
nav: true
nav_order: 3
---

## <b style="font-weight:800;">Log In</b>
###### Don't have an account yet? <a href="#Sign Up">Sign Up.</a>

<form action="{{ site.baseurl }}/spotify_search.html" method="get" id="search-ui">
  <!-- <label for="search-box">Search: </label> -->
  <input type="text" class="search-box" name="query" placeholder="Username" target="">
  <br />
  <input type="password" class="search-box" name="query" placeholder="Password"  target="">
  <button type="submit">
    <i class="fas fa-arrow-right"></i>
  </button>
  <!-- <input type="submit" value="🔍" id="search-button"> -->
</form>



<br /><br /><br /><br /><br />
## <a style="font-weight:800;margin-bottom:1rem;">Sign Up</a>
###### <b style="font-weight:400;">E-MAIL / 電子メール</b>
<input type="text" class="search-box" name="query" placeholder="Username">
<br />
<input type="password" class="search-box" name="query" placeholder="Password">
<button type="submit">
  <i class="fas fa-arrow-right"></i>
</button>


<br /><br />

###### <b style="font-weight:400;">PHONE NUMBER / 電話番号</b>
This is used for two-step verification. Your phone number will not be stored, or sold to third parties (as far as you are concerned).<br />
<input type="number" class="search-box" name="query" placeholder="Phone Number">
<button type="submit">
  <i class="fas fa-arrow-right"></i>
</button>


<br /><br /><br />
---