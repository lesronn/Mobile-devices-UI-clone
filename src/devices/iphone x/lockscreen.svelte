<script>
  import IoIosWifi from "svelte-icons/io/IoIosWifi.svelte";
  import IoIosBatteryFull from "svelte-icons/io/IoIosBatteryFull.svelte";
  import FaSignal from "svelte-icons/fa/FaSignal.svelte";
  import TiCamera from "svelte-icons/ti/TiCamera.svelte";
  import IoIosFlashlight from "svelte-icons/io/IoIosFlashlight.svelte";

  let currentime;
  setInterval(function () {
    let date = new Date();
    var time = date.toLocaleTimeString([], {
      timeStyle: "short",
      hour12: false,
    });
    currentime = time;
  }, 10);

  var date = new Date();
  let currentdate = date.toLocaleString("default", {
    month: "long",
    weekday: "long",
    day: "2-digit",
  });
</script>

<div class="lockscreen">
  <div class="notificationarea">
    <div class="time">MTN</div>
    <div class="batteryside">
      <div class="network"><FaSignal /></div>
      <div class="wifi"><IoIosWifi /></div>
      <div class="battery"><IoIosBatteryFull /></div>
    </div>
  </div>
  <div class="top">
    <div class="lockicon">
      <img src="/images/icons/lock.png" alt="" />
    </div>
    <div class="time">{currentime}</div>
    <div class="date">{currentdate}</div>
  </div>
  <div class="message">
    <div class="messagehead">
      <div class="left">
        <img src="/images/icons/imessage.png" alt="" />
        <div class="mtitle">messages</div>
      </div>
      <div class="right">now</div>
    </div>
    <div class="messagename">Macho</div>
    <div class="messagebody">
      Yo Lesron the man come class look sharp then come❗
    </div>
  </div>
  <div class="home">
    <p>swipe up to open</p>
    <div class="homeswipe" />
  </div>
  <div class="bottomicons">
    <div class="flashlighticon"><IoIosFlashlight /></div>
    <div class="cameraicon"><TiCamera /></div>
  </div>

  <!-- <div class="bat">
      <div class="batlevel" style="width: {batterypercentage};" />
    </div> -->
</div>

<style>
  .lockscreen .top {
    display: flex;
    flex-direction: column;
    width: 100%;
    justify-content: center;
    align-items: center;
    margin-top: 5px;
    color: white;
    font-family: "sflight";
  }
  .lockscreen .top .lockicon img {
    height: 36px;
    width: 36px;
  }
  .lockscreen .top .time {
    font-size: 35pt;
    font-weight: lighter;
    padding-top: 2px;
  }
  .lockscreen .top .date {
    padding-top: 2px;
  }
  .lockscreen .message {
    margin: 0px 7px;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 10px;
    margin-top: 25px;
    padding: 7px;
  }
  .lockscreen .message .messagehead {
    display: flex;
    width: 100%;
    justify-content: space-between;
  }
  .lockscreen .message .messagehead .right {
    font-size: 10px;
    mix-blend-mode: overlay;
  }
  .lockscreen .message .messagehead .left {
    text-transform: uppercase;
    display: flex;
  }
  .lockscreen .message .messagehead .left .mtitle {
    font-size: 10px;
    padding-left: 3px;
    mix-blend-mode: overlay;
  }
  .lockscreen .message .messagehead .left img {
    height: 13px;
    width: 13px;
    margin-right: 2px;
  }
  .lockscreen .message .messagename {
    font-weight: bold;
    font-size: 9pt;
    padding-top: 5px;
  }
  .lockscreen .message .messagebody {
    font-size: 9pt;
  }
  .bat {
    height: 5px;
    width: 10pt;
    border-radius: 2px;
    border: 2px solid white;
    position: absolute;
  }
  .batlevel {
    height: 100%;
    background: green;
  }
  .bat:after {
    content: "";
    height: 4px;
    width: 3px;
    background: #ffffff;
    position: absolute;
    left: 100%;
    top: 20%;
    border-radius: 1px;
  }
  .lockscreen .notificationarea {
    font-size: 8pt;
    font-weight: bold;
    color: #ffffff;
    width: 100%;
    display: flex;
    justify-content: space-between;
    padding: 8px 10px;
  }
  .lockscreen .notificationarea .time {
    padding-left: 10px;
  }
  .lockscreen .notificationarea .batteryside {
    display: flex;
    padding-right: 20px;
  }
  .lockscreen .notificationarea .batteryside .network {
    color: #ffffff;
    width: 10pt;
  }
  .lockscreen .notificationarea .batteryside .wifi {
    color: #ffffff;
    width: 10pt;
    padding: 0px 3px;
  }
  .lockscreen .notificationarea .batteryside .battery {
    color: #ffffff;
    width: 10pt;
  }
  .lockscreen .bottomicons {
    position: absolute;
    bottom: 0;
    display: flex;
    width: 100%;
    justify-content: space-between;
    margin-bottom: 40px;
  }
  .lockscreen .home {
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    transition: all 0.2s linear;
    margin-bottom: 15px !important;
  }

  .lockscreen .home p {
    color: rgb(250, 250, 250);
    margin-bottom: 10px;
    font-size: 12.5px;
    transition: all 0.2s linear;
    opacity: 0;
  }
  .lockscreen .home:hover p {
    opacity: 1;
  }
  .lockscreen:hover .homeswipe {
    opacity: 1;
  }
  .lockscreen .homeswipe {
    width: 100px;
    background: white;
    height: 4px;
    border-radius: 2px;
    opacity: 0;
    transition: all 0.3s linear !important;
  }

  .lockscreen .bottomicons .flashlighticon {
    width: 17pt;
    height: 17pt;
    color: white;
    padding: 7px;
    background: rgba(0, 0, 0, 0.4);
    margin-left: 20px;
    border-radius: 100%;
    justify-content: center;
    display: flex;
    align-items: center;
  }
  .lockscreen .bottomicons .cameraicon {
    width: 17pt;
    height: 17pt;
    color: white;
    padding: 7px;
    background: rgba(0, 0, 0, 0.4);
    margin-right: 20px;
    border-radius: 100%;
    justify-content: center;
    display: flex;
    align-items: center;
  }
</style>
