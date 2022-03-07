<script>
  import IoIosWifi from "svelte-icons/io/IoIosWifi.svelte";
  import IoIosBatteryFull from "svelte-icons/io/IoIosBatteryFull.svelte";
  import FaSignal from "svelte-icons/fa/FaSignal.svelte";
  import IoIosStar from "svelte-icons/io/IoIosStar.svelte";
  import MdWatchLater from "svelte-icons/md/MdWatchLater.svelte";
  import FaRegUserCircle from "svelte-icons/fa/FaRegUserCircle.svelte";
  import IoIosKeypad from "svelte-icons/io/IoIosKeypad.svelte";
  import MdVoicemail from "svelte-icons/md/MdVoicemail.svelte";
  let currentime;
  setInterval(function () {
    let date = new Date();
    var time = date.toLocaleTimeString([], {
      timeStyle: "short",
      hour12: false,
    });
    currentime = time;
  }, 1000);
</script>

<div class="phoneapp">
  <div class="notificationarea">
    <div class="time">{currentime}</div>
    <div class="batteryside">
      <div class="network"><FaSignal /></div>
      <div class="wifi"><IoIosWifi /></div>
      <!-- <div style="font-size: 9px; padding: 0px 3px; padding-top:1px;">LTE</div> -->
      <div class="battery"><IoIosBatteryFull /></div>
    </div>
  </div>

  <div class="tabbar">
    <div class="tabs">
      <div class="tab">
        <div class="icon"><IoIosStar /></div>
        <span class="tabname">favorites</span>
      </div>
      <div class="tab">
        <div class="icon"><MdWatchLater /></div>
        <span class="tabname">Recents</span>
      </div>
      <div class="tab">
        <div class="icon"><FaRegUserCircle /></div>
        <span class="tabname">Contacts</span>
      </div>
      <div class="tab">
        <div class="icon active"><IoIosKeypad /></div>
        <span class="tabname">keypad</span>
      </div>

      <div class="tab">
        <div class="icon "><MdVoicemail /></div>
        <span class="tabname">Voicemail</span>
      </div>
    </div>
  </div>
</div>

<style>
  .phoneapp {
    height: 100%;
    width: 100%;
    background: white;
  }
  .notificationarea {
    font-size: 8pt;
    font-weight: bold;
    color: black;
    width: 100%;
    display: flex;
    justify-content: space-between;
    padding: 8px 10px;
  }
  .notificationarea .time {
    padding-left: 10px;
    color: black;
  }
  .notificationarea .batteryside {
    display: flex;
    padding-right: 20px;
    color: black;
  }
  .notificationarea .batteryside .network {
    color: black;
    width: 10pt;
  }

  .notificationarea .batteryside .wifi {
    color: black;
    width: 10pt;
    padding: 0px 3px;
  }
  .notificationarea .batteryside .battery {
    color: black;
    width: 10pt;
  }

  .phoneapp .tabbar {
    width: 100%;
    height: 60px;
    position: absolute;
    bottom: 0;
    background: blue;
  }
  .phoneapp .tabbar .tabs {
    display: flex;
    width: 100%;
    height: 100%;
    justify-content: space-evenly;
    align-items: center;
  }
  .phoneapp .tabbar .tabs .icon {
    height: 18px;
    width: 18px;
  }
  .phoneapp .tabbar .tabs .tab {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-bottom: 15px;
  }
  .phoneapp .tabbar .tabs .tab .tabname {
    font-size: 9px;
  }
</style>
