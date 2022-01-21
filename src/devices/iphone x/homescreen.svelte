<script>
  import Notificationarea from "./notificationarea.svelte";
  import { onMount } from "svelte";
  import FaListUl from "svelte-icons/fa/FaListUl.svelte";
  import Carousel from "svelte-carousel";
  let screen = true;

  let carousel; // for calling methods of the carousel instance
  const handleNextClick = () => {
    carousel.goToNext();
  };
</script>

<div class="homescreen">
  <!-- <Notificationarea /> -->
  <Carousel bind:this={carousel} arrows={false} swiping={true} infinite={false}>
    <div class="icons">
      <div class="icons_container">
        <div class="row">
          <div class="widgets">
            <div class="reminder">
              <div class="rtop">
                <div class="rbtn"><FaListUl /></div>
                <span class="rnumber">0</span>
              </div>
              <div class="rbottom">
                <b>Remainders</b><br />
                <span>No Remainders</span>
              </div>
            </div>
            <div class="music">
              <div class="musictop">
                <img class="thumbnail" src="/images/misc.jpeg" alt="" />
                <img class="micon" src="/images/micon.png" alt="" />
              </div>
              <div class="musicdown">
                <b>Touch It</b>
                <br />
                <span>KiDi</span>
              </div>
            </div>
          </div>
        </div>
        <div class="row firstrow">
          <div class="appiconname">
            <img src="/images/icons/facetime.png" alt="" />
            <span>Facetime</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/call.png" alt="" />
            <span>Phone</span>
          </div>

          <div class="appiconname">
            <img src="/images/icons/photos.png" alt="" />
            <span>Photos</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/camera.png" alt="" />
            <span>Camera</span>
          </div>
        </div>
        <div class="row">
          <div class="appiconname">
            <img src="/images/icons/mail.png" alt="" />
            <span>Mail</span>
          </div>

          <div class="appiconname">
            <img src="/images/icons/clock.png" alt="" />
            <span>clock</span>
          </div>

          <div class="appiconname">
            <img src="/images/icons/mapp.png" alt="" />
            <span>Maps</span>
          </div>

          <div class="appiconname">
            <img src="/images/icons/weather.png" alt="" />
            <span>Weather</span>
          </div>
        </div>
        <div class="row">
          <div class="appiconname">
            <img src="/images/icons/reminder.png" alt="" />
            <span>reminder</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/notes.png" alt="" />
            <span>Notes</span>
          </div>

          <div class="appiconname">
            <img src="/images/icons/books.png" alt="" />
            <span>Books</span>
          </div>

          <div class="appiconname">
            <img src="/images/icons/appstore.png" alt="" />
            <span>App Store</span>
          </div>
        </div>
        <div class="row">
          <div class="appiconname">
            <img src="/images/icons/health.png" alt="" />
            <span>Health</span>
          </div>

          <div class="appiconname">
            <img src="/images/icons/home.png" alt="" />
            <span>Home</span>
          </div>

          <div class="appiconname">
            <img src="/images/icons/appletv.png" alt="" />
            <span> Tv</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/settings.png" alt="" />
            <span>settings</span>
          </div>
        </div>
      </div>
    </div>

    <div class="icons">
      <div class="icons_container">
        <div class="row">
          <div class="appiconname">
            <img src="/images/icons/files.png" alt="" />
            <span>files</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/find.png" alt="" />
            <span>Find My</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/compass.png" alt="" />
            <span> Compass</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/shortcuts.png" alt="" />
            <span>Shortcuts</span>
          </div>
        </div>
        <div class="row">
          <div class="appiconname">
            <img src="/images/icons/contacts.png" alt="" />
            <span>Contacts</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/calculator.png" alt="" />
            <span>Calculator</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/tips.png" alt="" />
            <span>Tips</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/measure.png" alt="" />
            <span>Measure</span>
          </div>
        </div>
        <div class="row">
          <div class="appiconname">
            <img src="/images/icons/podcast.png" alt="" />
            <span>Podcast</span>
          </div>

          <div class="appiconname">
            <img src="/images/icons/stocks.png" alt="" />
            <span>Stocks</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/imessage.png" alt="" />
            <span>Imessage</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/voice.png" alt="" />
            <span>voice</span>
          </div>
        </div>
        <div class="row">
          <div class="appiconname">
            <img src="/images/icons/wallet.png" alt="" />
            <span>Wallet</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/news.png" alt="" />
            <span>News</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/safari.png" alt="" />
            <span>safari</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/music15.png" alt="" />
            <span>music</span>
          </div>
        </div>
        <div class="row">
          <div class="appiconname">
            <img src="/images/icons/snapchat.png" alt="" />
            <span>snapchat</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/twitter.png" alt="" />
            <span>twitter</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/instagram.png" alt="" />
            <span>instagram</span>
          </div>
          <div class="appiconname">
            <img src="/images/icons/whatsapp.png" alt="" />
            <span>Whatsapp</span>
          </div>
        </div>
      </div>
    </div>
  </Carousel>

  <div class="appbar">
    <div class="appicons">
      <img src="/images/icons/call.png" alt="" />
      <img src="/images/icons/safari.png" alt="" />
      <img src="/images/icons/imessage.png" alt="" />
      <img src="/images/icons/music15.png" alt="" />
    </div>
  </div>
</div>

<style>
  .homescreen {
    height: 100vh !important;
    width: 100%;
  }

  .homescreen .icons {
    width: 100%;
    display: flex;
  }
  .homescreen .icons .icons_container {
    width: 100%;
    display: flex;
    flex-direction: column;
    margin: 5px 20px;
  }
  .homescreen .icons .row {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-bottom: 10px;
  }
  .homescreen .icons .firstrow {
    margin-top: 15px;
  }
  .homescreen .icons .appiconname {
    font-size: 10px;
    text-align: center;
    display: flex;
    flex-direction: column;
    color: white;
  }
  .homescreen .icons .appiconname span {
    padding-top: 2px;
    text-transform: capitalize;
  }

  .homescreen .icons img {
    height: 40px;
    width: 40px;
    cursor: pointer;
    -webkit-user-drag: none;
    -khtml-user-drag: none;
    -moz-user-drag: none;
    -o-user-drag: none;
    user-drag: none;
  }
  .homescreen .icons .row .widgets {
    width: 100%;
    display: flex;
    gap: 10px;
    justify-content: space-between;
  }
  .homescreen .icons .row .widgets .reminder {
    background: white;
    width: 100%;
    padding: 10px;
    flex: 50%;
    display: flex;
    flex-direction: column;
    border-radius: 10px;
    justify-content: space-between;
  }
  .homescreen .icons .row .widgets .reminder:after {
    content: "Reminder";
    position: absolute;
    margin-top: 92px;
    font-size: 10px;
    text-align: center !important;
    color: white;
    padding-left: 19px;
  }
  .homescreen .icons .row .widgets .reminder .rtop {
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: space-between;
    align-items: center;
  }
  .homescreen .icons .row .widgets .reminder .rtop .rbtn {
    height: 12px;
    width: 12px;
    padding: 6px;
    border-radius: 50%;
    justify-content: center;
    align-items: center;
    color: white;
    display: flex;
    background: #0b77f6;
  }
  .homescreen .icons .row .widgets .reminder .rtop .rnumber {
    font-weight: bold;
    font-size: 18px;
  }
  .homescreen .icons .row .widgets .reminder .rbottom b {
    color: #0b77f6;
    font-size: 12px;
  }
  .homescreen .icons .row .widgets .reminder .rbottom {
    line-height: 13px;
  }
  .homescreen .icons .row .widgets .reminder .rbottom span {
    color: grey;
    font-size: 10px;
  }

  .homescreen .icons .row .widgets .music {
    background: white;
    width: 100%;
    padding: 8px;
    flex: 50%;
    display: flex;
    flex-direction: column;
    border-radius: 10px;
  }

  .homescreen .icons .row .widgets .music:after {
    content: "Music";
    position: absolute;
    margin-top: 94px;
    font-size: 10px;
    text-align: center !important;
    color: white;
    padding-left: 25px;
  }
  .homescreen .icons .row .widgets .music .musictop {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;
  }
  .homescreen .icons .row .widgets .music .thumbnail {
    border-radius: 5px;
    height: 47px;
    width: 47px;
  }
  .homescreen .icons .row .widgets .music .micon {
    height: 13px;
    width: 13px;
  }

  .homescreen .icons .row .widgets .music .musicdown {
    line-height: 12px;
    margin-top: 10px;
  }
  .homescreen .icons .row .widgets .music .musicdown b {
    font-size: 12px;
  }
  .homescreen .icons .row .widgets .music .musicdown span {
    font-size: 10px;
    color: tomato;
  }
  .homescreen .appbar {
    position: absolute;
    bottom: 0;
    display: flex;
    width: 100%;
  }
  .homescreen .appbar .appicons {
    width: 100%;
    height: 60px;
    background: rgba(255, 255, 255, 0.2);
    margin: 0px 10px 10px 10px;
    border-radius: 20px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-evenly;
  }
  .homescreen .appbar .appicons img {
    height: 40px;
    width: 40px;
    cursor: pointer;
  }
</style>
