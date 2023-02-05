---
layout: page
permalink: /login/
title: Log In / Sign Up
description: Log in to an existing account, or create a new account.
nav: true
nav_order: 3
---

<div class="card mt-3 wow fadeIn" data-wow-delay="1s" style="padding: 3rem;">
  <h2><b style="font-weight:800;">Log In</b></h2>
  <h6>Don't have an account yet? <a href="#Sign Up">Sign Up.</a></h6>
  <form action="{{ site.baseurl }}/spotify_search.html" method="get" id="search-ui">
    <!-- <label for="search-box">Search: </label> -->
    <i class="fas fa-user"></i> <input type="text" class="search-box" name="query" placeholder="👤 Username" target="">
    <br />
    <i class="fas fa-unlock"></i> <input type="password" class="search-box" name="query" placeholder="🔑 Password"  target="">
    <button type="submit">
      <i class="fas fa-arrow-right"></i>
    </button>
    <!-- <input type="submit" value="🔍" id="search-button"> -->
  </form>
</div>

<br /><br />
<div class="card mt-3 wow fadeIn" data-wow-delay="1s" style="padding: 3rem;">
  <h2><a style="font-weight:800;margin-bottom:1rem;">Sign Up</a></h2>
  <h6><b style="font-weight:400;"><i class="fas fa-at"></i> E-MAIL / 電子メール</b></h6>
  <form action="{{ site.baseurl }}/search.html" method="get" id="search-ui">
    <!-- <label for="search-box">Search: </label> -->
    <i class="fas fa-user"></i> <input type="text" class="search-box" name="query" placeholder="👤 Create Username" target="">
    <br />
    <i class="fas fa-unlock"></i> <input type="password" class="search-box" name="query" placeholder="🔑 Create Password"  target="">
    <button type="submit">
      <i class="fas fa-arrow-right"></i>
    </button>
    <!-- <input type="submit" value="🔍" id="search-button"> -->
  </form>
  <br /><br /><br />
  <h6><b style="font-weight:400;"><i class="fas fa-phone"></i> PHONE NUMBER / 電話番号</b></h6>
  This is used for two-step verification, and alerts. Your phone number will not be stored, or sold to third parties.<br /><br />

  <form action="{{ site.baseurl }}/search.html" method="get" id="search-ui">
    <!-- <label for="search-box">Search: </label> -->
    <i class="fas fa-mobile"></i> <input type="text" class="search-box" name="query" placeholder="📞 Phone Number" target=""><br /><br /><br />
    <h6><b style="font-weight:400;"><i class="fas fa-phone"></i> ADDRESS / 電話番号</b></h6>
    <input type="text" class="search-box" name="query" placeholder="🏠 House Number" target=""><br />
    <input type="text" class="search-box" name="query" placeholder="🏘 Address 1" target=""><br />
    <input type="text" class="search-box" name="query" placeholder="🏘 Address 2" target=""><br />
    <input type="text" class="search-box" name="query" placeholder="📮 Postcode" target="">
    <br /><br /><br />
    <h6><b style="font-weight:400;"><i class="fas fa-phone"></i> DIETARY REQUIREMENTS / 電話番号</b></h6>
    <select name="allergies" id="allergies" class="search-box" target="" onchange="dropdownChange();">
      <option value="none">🍲 No Allergy Requirements</option>
      <option value="nuts">Nuts</option>
      <option value="crustacean">Crustacean</option>
      <option value="lactose">Lactose</option>
      <option value="eggs">Eggs</option>
      <option value="wheat">Wheat</option>
      <option value="gluten">Gluten</option>
      <option value="soy">Soy</option>
      <option value="fish">Fish</option>
      <option value="other">Other</option>
    </select>
    <br />
    <select name="dietary" id="dietary" class="search-box" target="" onchange="dropdownChange();">
      <option value="none">🍲 No Dietary Requirements</option>
      <option value="vegetarian">🍆 Vegetarian</option>
      <option value="vegan">🍆 Vegan</option>
      <option value="halal">☪ Halal</option>
      <option value="kosher">✡ Kosher</option>
      <option value="other">Other</option>
    </select>
    <button type="submit"><i class="fas fa-arrow-right"></i></button>
      <!-- <input type="submit" value="🔍" id="search-button"> -->
    </form>
    <br /><br />

  <p>
    <a class="btn btn-primary" data-toggle="collapse" href="#multiCollapseExample1" role="button" aria-expanded="false" aria-controls="multiCollapseExample1">Click if "Other"</a>
  </p>
  <div class="row">
    <div class="col">
      <div class="collapse multi-collapse" id="multiCollapseExample1">
        <div class="card card-body">
          <h4>Click the submit button above, if "Other" has been chosen.</h4>
          <input type="text" class="search-box" id="other-allergies" name="query" placeholder="🍲 Other Allergies" target="">
          <br />
          <input type="text" class="search-box" id="other-dietary" name="query" placeholder="🍲 Other Dietary Requirements" target="">
        </div>
      </div>
    </div>
  </div>


  <br /><br /><br />
  <h6><b style="font-weight:400;"><i class="fab fa-spotify"></i> SPOTIFY INTEGRATION・</b></h6>
  Integrate your Spotify account.<br /><br />
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
</div>
<br /><br />

---