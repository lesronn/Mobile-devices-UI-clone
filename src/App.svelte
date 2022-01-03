<script>
  /*** IMPORT STATEMENTS ***/
  import IoIosWifi from "svelte-icons/io/IoIosWifi.svelte";
  import IoIosBatteryFull from "svelte-icons/io/IoIosBatteryFull.svelte";
  import FaSignal from "svelte-icons/fa/FaSignal.svelte";
  import TiCamera from "svelte-icons/ti/TiCamera.svelte";
  import IoIosFlashlight from "svelte-icons/io/IoIosFlashlight.svelte";
  import FaLock from "svelte-icons/fa/FaLock.svelte";

  const home = () => {
    console.log("You just dragged me");
  };
  let batterypercentage;

  navigator.getBattery().then(function (battery) {
    batterypercentage = battery.level * 100 + "%";
    console.log(batterypercentage);
  });

  let currentime;
  setInterval(function () {
    let date = new Date();
    var time = date.toLocaleTimeString([], {
      timeStyle: "short",
      hour12: false,
    });
    currentime = time;
  }, 1000);

  var date = new Date();
  let currentdate = date.toLocaleString("default", {
    month: "long",
    weekday: "long",
    day: "2-digit",
  });
</script>

<div class="iphone">
  <div class="screen">
    <div class="notificationarea">
      <div class="time">MTN</div>
      <div class="batteryside">
        <div class="network"><FaSignal /></div>
        <div class="wifi"><IoIosWifi /></div>
        <div class="battery"><IoIosBatteryFull /></div>
      </div>
    </div>
    <div class="top">
      <div class="lockicon"><img src="/images/icons/lock.png" alt="" /></div>
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
      <p>swipe up to unlock</p>
      <div class="homeswipe" on:drag={home} />
    </div>
    <div class="bottomicons">
      <div class="flashlighticon"><IoIosFlashlight /></div>
      <div class="cameraicon"><TiCamera /></div>
    </div>

    <!-- <div class="bat">
      <div class="batlevel" style="width: {batterypercentage};" />
    </div> -->
  </div>
  <div class="notch">
    <div class="mouthpiece" />
    <div class="camera" />
  </div>
  <div class="silentswicth" />
  <div class="volume">
    <div class="volup" />
    <div class="voldown" />
  </div>
  <div class="powerbtn" />
</div>

<style>
  .iphone {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(1.2);
    width: 280px;
    height: 540px;
    background: #ffffff;
    border-radius: 35px;
    box-shadow: inset 0 0 15px rgba(0, 0, 0, 0.2),
      0 40px 100px rgba(0, 0, 0, 0.4);
    transition: 0.5s;
    z-index: 99;
  }
  .iphone .screen {
    position: absolute;
    top: 15px;
    left: 15px;
    width: calc(100% - 30px);
    height: calc(100% - 30px);
    background-image: url("/images/wallpapers/default1.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    border-radius: 25px;
    box-shadow: inset 0 0 20px rgba(0, 0, 0, 0.2);
    cursor: grab;
  }
  .iphone .screen .top {
    display: flex;
    flex-direction: column;
    width: 100%;
    justify-content: center;
    align-items: center;
    margin-top: 5px;
    color: white;
    font-family: "sflight";
  }
  .iphone .screen .top .lockicon img {
    height: 36px;
    width: 36px;
  }
  .iphone .screen .top .time {
    font-size: 35pt;
    font-weight: lighter;
    padding-top: 2px;
  }
  .iphone .screen .top .date {
    padding-top: 2px;
  }
  .iphone .screen .message {
    margin: 0px 7px;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 10px;
    margin-top: 25px;
    padding: 7px;
  }
  .iphone .screen .message .messagehead {
    display: flex;
    width: 100%;
    justify-content: space-between;
  }
  .iphone .screen .message .messagehead .right {
    font-size: 10px;
    mix-blend-mode: overlay;
  }
  .iphone .screen .message .messagehead .left {
    text-transform: uppercase;
    display: flex;
  }
  .iphone .screen .message .messagehead .left .mtitle {
    font-size: 10px;
    padding-left: 3px;
    mix-blend-mode: overlay;
  }
  .iphone .screen .message .messagehead .left img {
    height: 13px;
    width: 13px;
    margin-right: 2px;
  }
  .iphone .screen .message .messagename {
    font-weight: bold;
    font-size: 9pt;
    padding-top: 5px;
  }
  .iphone .screen .message .messagebody {
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
  .iphone .screen .notificationarea {
    font-size: 8pt;
    font-weight: bold;
    color: #ffffff;
    width: 100%;
    display: flex;
    justify-content: space-between;
    padding: 8px 10px;
  }
  .iphone .screen .notificationarea .time {
    padding-left: 10px;
  }
  .iphone .screen .notificationarea .batteryside {
    display: flex;
    padding-right: 20px;
  }
  .iphone .screen .notificationarea .batteryside .network {
    color: #ffffff;
    width: 10pt;
  }
  .iphone .screen .notificationarea .batteryside .wifi {
    color: #ffffff;
    width: 10pt;
    padding: 0px 3px;
  }
  .iphone .screen .notificationarea .batteryside .battery {
    color: #ffffff;
    width: 10pt;
  }
  .iphone .screen .bottomicons {
    position: absolute;
    bottom: 0;
    display: flex;
    width: 100%;
    justify-content: space-between;
    margin-bottom: 40px;
  }
  .iphone .screen .home {
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    transition: all 0.2s linear;
    margin-bottom: 15px !important;
  }

  .iphone .screen .home p {
    color: rgb(250, 250, 250);
    margin-bottom: 10px;
    font-size: 12.5px;
    transition: all 0.2s linear;
    opacity: 0;
  }
  .iphone .screen .home:hover p {
    opacity: 1;
  }
  .iphone .screen:hover .homeswipe {
    opacity: 1;
  }
  .iphone .screen .homeswipe {
    width: 100px;
    background: white;
    height: 4px;
    border-radius: 2px;
    opacity: 0;
    transition: all 0.3s linear !important;
  }

  .iphone .screen .bottomicons .flashlighticon {
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
  .iphone .screen .bottomicons .cameraicon {
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

  .iphone .notch {
    position: absolute;
    top: 14px;
    left: 50%;
    width: 130px;
    transform: translateX(-50%);
    height: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #fff;
    border-bottom-left-radius: 10px;
    border-bottom-right-radius: 10px;
  }
  .iphone .notch .camera {
    height: 10px;
    width: 10px;
    border-radius: 50%;
    background: #262626;
    /* margin-right: 10px; */
  }
  .iphone .notch .mouthpiece {
    height: 5px;
    width: 50px;
    background: #262626;
    border-radius: 2px;
    margin-right: 10px;
  }
  .iphone .silentswicth {
    position: absolute;
    top: 12%;
    right: 100%;
    width: 3px;
    height: 15px;
    background: white;
    border-top-left-radius: 2px;
    border-bottom-left-radius: 2px;
  }
  .iphone .volume {
    position: absolute;
    top: 20%;
    right: 101.5%;
  }
  .iphone .volume .volup {
    position: inherit;
    width: 4px;
    height: 30px;
    background: white;
    border-top-left-radius: 3px;
    border-bottom-left-radius: 3px;
    cursor: pointer;
  }
  .iphone .volume .voldown {
    position: inherit;
    width: 4px;
    height: 30px;
    background: white;
    border-top-left-radius: 3px;
    border-bottom-left-radius: 3px;
    margin-top: 40px;
    cursor: pointer;
  }
  .iphone .powerbtn {
    position: absolute;
    top: 20%;
    left: 100%;
    width: 4px;
    height: 70px;
    background: white;
    border-top-right-radius: 3px;
    border-bottom-right-radius: 3px;
    cursor: pointer;
  }
</style>
