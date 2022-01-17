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
        <div class="row">
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
        </div>
        <div class="row">
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
        </div>
        <div class="row">
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
        </div>
        <div class="row">
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
        </div>
      </div>
    </div>

    <div class="icons">
      <div class="icons_container">
        <div class="row">
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
        </div>
        <div class="row">
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
        </div>
        <div class="row">
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
        </div>
        <div class="row">
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
        </div>
        <div class="row">
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
          <img src="/images/icons/call.png" alt="" />
        </div>
      </div>
    </div>
  </Carousel>

  <div class="appbar">
    <div class="appicons">
      <img src="/images/icons/call.png" alt="" />
      <img src="/images/icons/safari.png" alt="" />
      <img src="/images/icons/imessage.png" alt="" />
      <img src="/images/icons/music.png" alt="" />
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
    margin: 10px 20px;
  }
  .homescreen .icons .row {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-bottom: 20px;
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
  .homescreen .icons .row .widgets .music .musictop {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;
  }
  .homescreen .icons .row .widgets .music .thumbnail {
    border-radius: 5px;
    height: 55px;
    width: 55px;
  }
  .homescreen .icons .row .widgets .music .micon {
    height: 16px;
    width: 16px;
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
