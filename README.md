<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kai's Profile</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Play&display=swap');

:root {
  --bg: #000;
  --cyan: #C4F6FF;
  --border: #777;
  --box: #050505;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 0;
  background: var(--bg);
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Black_from_a_camera.jpg/1200px-Black_from_a_camera.jpg");
  background-attachment: fixed;
  background-size: 1000px;
  color: var(--cyan);
  font-family: 'Play', Arial, sans-serif;
  font-size: 13px;
  cursor: url("https://cur.cursors-4u.net/others/oth-1/oth3.png"), auto;
}

a {
  color: var(--cyan);
  font-weight: bold;
  text-decoration: underline;
}

a:hover {
  color: white;
}

img {
  max-width: 100%;
}

body::after {
  content: "";
  position: fixed;
  inset: 0;
  z-index: 20;
  pointer-events: none;
  background: linear-gradient(
    rgba(10, 10, 50, 0.2) 50%,
    transparent 50%
  );
  background-size: 100% 2px;
}

/* TOP NAVIGATION */

.top-nav {
  background: #000;
  border: 2px solid var(--border);
  padding: 10px;
  text-align: center;
  margin: 5px auto;
  max-width: 1000px;
}

.top-nav a {
  margin: 0 8px;
  color: var(--cyan);
}

/* MAIN LAYOUT */

.container {
  width: 95%;
  max-width: 1000px;
  margin: 15px auto;
  padding: 12px;
  display: grid;
  grid-template-columns: 300px 1fr;
  gap: 15px;
  background: #000;
  border: 2px solid var(--border);
}

.profile-box {
  background: var(--box);
  border: 2px solid var(--border);
  margin-bottom: 15px;
  animation: float 5s ease-in-out infinite;
}

.box-header {
  background: #000;
  color: var(--cyan);
  border-bottom: 2px solid var(--border);
  padding: 8px;
  font-weight: bold;
  font-size: 14px;
}

.box-content {
  padding: 10px;
  color: var(--cyan);
}

h1, h2, h3, h4, p, td {
  color: var(--cyan);
}

h1 {
  font-family: Courier, monospace;
  font-size: 20px;
  overflow: hidden;
  white-space: nowrap;
  animation: type 3s steps(20);
}

h2 {
  font-size: 19px;
}

/* PROFILE PICTURE */

.profile-pic {
  width: 190px;
  height: 190px;
  margin: 10px auto;
  border: 3px double var(--cyan);
  padding: 5px;
  background: #111;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  overflow: hidden;
}

.profile-pic img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* STATUS */

.status-box {
  border: 2px dashed var(--cyan);
  padding: 10px;
  margin-bottom: 15px;
  text-align: center;
  background: #080808;
}

/* FRIEND SPACE */

.friend-space {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
  text-align: center;
}

.friend-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 5px;
}

.friend-pic {
  width: 55px;
  height: 55px;
  background: #222;
  border: 1px solid var(--cyan);
}

/* MUSIC PLAYER */

.music-player {
  background: #000;
  color: var(--cyan);
  border: 2px solid var(--border);
  padding: 12px;
  margin-bottom: 15px;
  text-align: center;
  font-family: monospace;
}

/* STAMPS AND BLINKIES */

.stamp-wall {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  gap: 5px;
  padding: 8px;
}

.stamp-wall img {
  width: auto;
  max-width: 100%;
  height: auto;
  max-height: 100px;
  object-fit: contain;
  transition: 0.2s;
}

.stamp-wall img:hover {
  animation: shake 0.5s infinite;
}

.blinkie-wall {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 3px;
  padding: 8px;
}

.blinkie-wall img {
  width: 150px;
  max-width: 48%;
  height: auto;
}

/* BANNER */

.banner {
  width: 100%;
  height: 200px;
  background-image: url("https://i.pinimg.com/originals/d1/ce/15/d1ce15d284b3e347422df62818e09af6.gif");
  background-position: center;
  background-size: cover;
  border: 2px solid var(--border);
  margin-bottom: 15px;
}

/* DETAILS TABLE */

table {
  width: 100%;
  border-collapse: collapse;
}

td {
  padding: 7px;
  border: 1px solid var(--border);
  background: #000;
}

/* ANIMATIONS */

@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(5px); }
}

@keyframes shake {
  0% { transform: translate(1px, 1px) rotate(0deg); }
  20% { transform: translate(-2px, 0) rotate(1deg); }
  40% { transform: translate(2px, -1px) rotate(-1deg); }
  60% { transform: translate(-2px, 1px) rotate(0deg); }
  80% { transform: translate(1px, -1px) rotate(1deg); }
  100% { transform: translate(1px, 1px) rotate(0deg); }
}

@keyframes type {
  from { width: 0; }
  to { width: 20ch; }
}

/* FOOTER */

footer {
  background: #000;
  border: 2px solid var(--border);
  color: var(--cyan);
  text-align: center;
  padding: 15px;
  margin: 15px auto;
  max-width: 1000px;
}

/* MOBILE */

@media (max-width: 700px) {
  .container {
    grid-template-columns: 1fr;
    width: 96%;
  }

  .top-nav a {
    display: inline-block;
    margin: 5px;
  }

  .friend-space {
    grid-template-columns: repeat(4, 1fr);
  }

.banner {
  height: 130px;
}

/* Make all images black and white */
img {
  filter: grayscale(100%);
  transition: filter 0.3s ease;
}

img:hover {
  filter: grayscale(0%);
}

</style>

<body>

<!-- NAVIGATION -->

<div class="top-nav">
  <a href="#">Home</a> |
  <a href="#">Browse</a> |
  <a href="#">Search</a> |
  <a href="#">Invite</a> |
  <a href="#">Mail</a> |
  <a href="#">Blog</a>
</div>

<div class="container">

<!-- LEFT COLUMN -->

<div class="left-col">

<h1>Kai's Profile</h1>

<div class="profile-pic">
  <span>[ YOUR PROFILE PICTURE ]</span>
</div>

<div class="status-box">
  Mood: 🎸 Listening to music
  <br>
  <i>"welcome to my page"</i>
</div>

<!-- CONTACT -->

<div class="profile-box">
  <div class="box-header">Contacting Kai</div>
  <div class="box-content">
    <a href="https://pin.it/6woKylp2U" target="_blank">📌 Pinterest</a><br><br>
    <a href="https://open.spotify.com/user/0fk22qvy97rcgzpyzi2g61wzd" target="_blank">🎵 Spotify</a><br><br>
    <a href="https://www.instagram.com/1nkyr0s3" target="_blank">📷 Instagram</a><br><br>
    <a href="#">★ Add to Favorites</a>
  </div>
</div>
</div>

<!-- TOP 8 -->

<div class="profile-box">
  <div class="box-header">Kai's Friend Space (Top 8)</div>
  <div class="box-content">
    <div class="friend-space">

      <div class="friend-card">
        <div class="friend-pic"></div>
        <a href="#">Jewels</a>
      </div>

      <div class="friend-card">
        <div class="friend-pic"></div>
        <a href="#">🖤Cai🩷</a>
      </div>

      <div class="friend-card">
        <div class="friend-pic"></div>
        <a href="#">Alisha</a>
      </div>

      <div class="friend-card">
        <div class="friend-pic"></div>
        <a href="#">dexter</a>
      </div>

      <div class="friend-card">
        <div class="friend-pic"></div>
        <a href="#">LinkinPrk99</a>
      </div>

      <div class="friend-card">
        <div class="friend-pic"></div>
        <a href="#">Ruthie</a>
      </div>

      <div class="friend-card">
        <div class="friend-pic"></div>
        <a href="#">RetroCoder</a>
      </div>

      <div class="friend-card">
        <div class="friend-pic"></div>
        <a href="#">Glitch</a>
      </div>

    </div>
  </div>
</div>

</div>

<!-- RIGHT COLUMN -->

<div class="right-col">

<div class="banner"></div>

<!-- MUSIC -->

<div class="music-player">
  🎵 <b>NOW PLAYING</b> 🎵
  <br><br>
  <iframe
    style="border-radius:8px"
    src="https://open.spotify.com/embed/playlist/PLAYLIST_ID"
    width="100%"
    height="152"
    frameborder="0"
    allow="encrypted-media">
  </iframe>
</div>

<!-- ABOUT ME -->

<div class="profile-box">
  <div class="box-header">Kai's Blurbs</div>
  <div class="box-content">

    <h3>About Me:</h3>
    <p>
      Welcome to my profile!!
      <br>
      Music, art, old internet stuff, and random things.
    </p>

    <h3>Who I'd Like to Meet:</h3>
    <p>
      Music lovers, artists, and other people with cool profiles.
    </p>

  </div>
</div>

<!-- INTERESTS -->

<div class="profile-box">
  <div class="box-header">Interests & Details</div>
  <div class="box-content">
    <table>
      <tr>
        <td><b>General:</b></td>
        <td>Art, photography, internet nostalgia</td>
      </tr>
      <tr>
        <td><b>Music:</b></td>
        <td>Emo, rock, alternative, nu-metal and any music really</td>
      </tr>
      <tr>
        <td><b>Movies:</b></td>
        <td>Horror, psychological movies</td>
      </tr>
      <tr>
        <td><b>Hobbies:</b></td>
        <td>Drawing, music, coding</td>
      </tr>
    </table>
  </div>
</div>

<!-- STAMPS -->

<div class="profile-box">
  <div class="box-header">My Stamps ☆</div>
  <div class="box-content">
    <div class="stamp-wall">

      <img src="https://raining-starss.neocities.org/zn%20(2).gif" alt="Stamp">
      <img src="https://i.postimg.cc/Qdp5z9Yf/Rachel-Amber-Wink-Stamp.gif" alt="Rachel Amber wink">
      <img src="https://i.postimg.cc/gk4n5Cv6/Rachel-Amber-Finger-Gun-Stamp.gif" alt="Rachel Amber stamp">
      <img src="https://raining-starss.neocities.org/thebread%20(10).gif" alt="Stamp">
      <img src="https://i.postimg.cc/P5N9zH6f/Price-Field-Selfie-Stamp.gif" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/sH2vmjVruWHi4GIKZHEMGdwl3jecw-FlRFzqMKremS2M=/https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/28fb1909-cb86-4358-8ace-2ffee1c86b60/d29nol9-0021170a-670f-4b93-a05d-04af59c85486.png" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/sHh16Bnsm_pwffnW9_LkU4KybPD5G4w5QeoR7Yc0mnC0=/https://shishka.neocities.org/shishka/img/stamps/36.gif" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/sChYnU8GHKlIYGssz__prqiblSR6tyseBF1Yup-uhwko=/https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/i/0ea075a2-c302-41ab-b1af-124a52b187a6/d1183yn-3d1547c8-c1f5-49ed-adf3-fd63abcc231d.gif" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/s8C33KNyiPyrRXEu4Uarjir5url_LDfPqLrZAF7z97YE=/https://64.media.tumblr.com/9505c416803af2ef87a292241d84363d/56fefd3f1342a5c1-c4/s100x200/4ec204c90077250835a295ab66804f8aa0b79254.gifv" alt="Stamp">

      <img src="https://allyratworld.com/stamps/d9rz26g-fb071f9e-c4f2-4083-82fc-41d9f36a92e0.png" alt="Stamp">

      <img src="https://i.postimg.cc/vHBK7MBq/Kate-Hug-Stamp.gif" alt="Kate hug stamp">
      <img src="https://i.postimg.cc/2SxTgKVb/LIS-Tempeststamp.gif" alt="Life is Strange stamp">

      <img src="https://i.ibb.co/RjBdSrQ/tumblr-03d1ef9137e1966107f981e5a63729b4-106ac2e0-100.webp" alt="Stamp">
      <img src="https://i.ibb.co/5jmskMp/tumblr-d970cac53516f88e229c5a5aba5600ac-2bce6be9-100.png" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/svZArcjFUMwADw8R1qDlLAV9mXgJDZdvCvZkJqP85DNg=/https://i.postimg.cc/QCBqwT7n/f181b293.gif" alt="Stamp">

      <img src="https://raining-starss.neocities.org/s2%20(2).jpg" alt="Stamp">
      <img src="https://raining-starss.neocities.org/s2%20(1).jpg" alt="Stamp">
      <img src="https://raining-starss.neocities.org/i_support_spinning_by_dinru.gif" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/sVcoHJyuvuNJ-1_oEn_ggzlA1WzcgBpcN_NEklnjD3aI=/https://64.media.tumblr.com/4e181b719f39a2500f3c4ab15cff5609/tumblr_pt5ssvxGB71xzybrpo6_100.png" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/sGOAMEIMvUS-p_9qwWYOIuUMVlSBz_XxD6njClYOh-Wo=/https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/8d6eb24e-44be-4b57-9edf-0febfe170821/dg0obug-637c779b-4c06-4cbe-b541-370bc563b775.png" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/ssK-Z53QSWTd2oDZEn9OCn0kPufBmXOKzqT762qWsKq0=/https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/6ea2e59a-916e-4a16-af1b-188ecf984fcc/d4n1wi2-de8fee98-b8aa-4a10-8699-dc5d657b52b5.gif" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/sh5m8SC250c_76Ha6NRH5ra4wqx7rx0Yo6M9T5jg5Jck=/https://i.ibb.co/GWTzH3Z/cooleronline.gif" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/s64jRcf2stXlWuGDPe3iNyrSWXwsuBQV7bxPTlwsRpQY=/https://64.media.tumblr.com/18b79994ab5cbabe4d2ef7a95ee6d96a/tumblr_pz7t3br6eb1xzybrpo6_250.gifv" alt="Stamp">

      <img src="https://raining-starss.neocities.org/s2%20(11).gif" alt="Stamp">
      <img src="https://raining-starss.neocities.org/73119stamps%20(1).png" alt="Stamp">
      <img src="https://raining-starss.neocities.org/73119stamps%20(4).png" alt="Stamp">
      <img src="https://raining-starss.neocities.org/d.gif" alt="Stamp">
      <img src="https://raining-starss.neocities.org/doot%20(6).png" alt="Stamp">
      <img src="https://raining-starss.neocities.org/doot%20(2).png" alt="Stamp">
      <img src="https://raining-starss.neocities.org/thebread%20(5).gif" alt="Stamp">
      <img src="https://raining-starss.neocities.org/plugplug%20(1).gif" alt="Stamp">
      <img src="https://raining-starss.neocities.org/thebread%20(2).png" alt="Stamp">
      <img src="https://raining-starss.neocities.org/goodieblink%20(13).png" alt="Stamp">
      <img src="https://raining-starss.neocities.org/goodieblink%20(3).png" alt="Stamp">
      <img src="https://raining-starss.neocities.org/dark%20(8).gif" alt="Stamp">
      <img src="https://raining-starss.neocities.org/t3%20(1).gif" alt="Stamp">
      <img src="https://raining-starss.neocities.org/t3%20(2).png" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/s6wHxpKyaqtS9-zEll525vqguxNfF9ZhntBnr90zbFYQ=/https://media1.tenor.com/m/6PiCEPCyWwYAAAAd/serena-mtv.gif" alt="Stamp">

      <img src="https://external-media.spacehey.net/media/sx-sOhIoY2ENiFODXyopkmqPrVBO3WSjilxF4U7cP7zw=/https://i.postimg.cc/tg4XsQkN/gerard-verysilly.png" alt="Gerard stamp">

    </div>
  </div>
</div>

<!-- BLINKIES -->

<div class="profile-box">
  <div class="box-header">Blinkies!!</div>
  <div class="box-content">
    <div class="blinkie-wall">

      <img src="https://blinkies.cafe/b/display/0275-stressed.gif" alt="Stressed">
      <img src="https://blinkies.cafe/b/display/0179-kittencry.gif" alt="Kitten cry">
      <img src="https://blinkies.cafe/b/display/0275-spiderweb.gif" alt="Spiderweb">
      <img src="https://blinkies.cafe/b/display/0277-zombies.gif" alt="Zombies">
      <img src="https://blinkies.cafe/b/display/0245-pikachuhearts.gif" alt="Pikachu hearts">
      <img src="https://blinkies.cafe/b/display/0250-redbouncyhearts.gif" alt="Red hearts">
      <img src="https://blinkies.cafe/b/display/0202-pinterestlogo.gif" alt="Pinterest">
      <img src="https://blinkies.cafe/b/display/0187-transparentsparkle.gif" alt="Sparkles">
      <img src="https://blinkies.cafe/b/display/0192-forgetmenotflower.gif" alt="Flowers">
      <img src="https://blinkies.cafe/b/display/0191-fallleaves.gif" alt="Fall leaves">
      <img src="https://blinkies.cafe/b/display/0143-webkinz.gif" alt="Webkinz">
      <img src="https://blinkies.cafe/b/display/0163-cherry.gif" alt="Cherry">
      <img src="https://blinkies.cafe/b/display/0147-kirbywalk.gif" alt="Kirby">
      <img src="https://blinkies.cafe/b/display/0144-pokeball.gif" alt="Pokeball">
      <img src="https://blinkies.cafe/b/display/0148-kirbyswim.gif" alt="Kirby">
      <img src="https://blinkies.cafe/b/display/0164-bloodylips.gif" alt="Blinkie">
      <img src="https://blinkies.cafe/b/display/0149-ty.gif" alt="Thank you">
      <img src="https://blinkies.cafe/b/display/0124-stars.gif" alt="Stars">
      <img src="https://blinkies.cafe/b/display/0221-cd.gif" alt="CD">

    </div>
  </div>
</div>

</div>
</div>

<footer>
  <p>Thanks for visiting my profile ☆</p>
  <p>Best viewed with nostalgia and loud music.</p>
</footer>

</body>
</html>
