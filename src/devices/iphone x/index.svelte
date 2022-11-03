<script>
  /*** IMPORT STATEMENTS ***/

  import Homescreen from "./homescreen.svelte";
  import Lockscreen from "./lockscreen.svelte";
  import Searchscreen from "./SearchScreen.svelte";
  import Notificationarea from "./notificationarea.svelte";
  import PhoneApp from "./apps/phone.svelte";

  let screen = true;
</script>

<div class="world">
  <div class="phone-side">
    <div class="iphone">
      <div class="screen">
        {#if screen}
          <!-- <PhoneApp /> -->
          <Homescreen />
          <!-- <Searchscreen /> -->
        {:else}
          <Lockscreen />
        {/if}
      </div>

      <div class="notch">
        <div class="mouthpiece" />
        <div class="camera">
          <div class="camera1" />
        </div>
      </div>
      <div class="silentswicth" />
      <div class="volume">
        <div class="volup" />
        <div class="voldown" />
      </div>
      <div class="powerbtn" />
    </div>
  </div>
  <div class="info-side">
    <div class="main-info">
      <h2>Mobile Ui Devices Clone</h2>
    </div>
    <marquee behavior="" direction="right">
      This app is still under development
    </marquee>
    <div class="info-side-footer">
      <p>
        Developed with ❤️ | by <a
          href="https://github.com/lesronn"
          target="_blank"><strong>Lesron</strong></a
        >.
      </p>
    </div>
  </div>
</div>

<style>
  .world {
    width: 100%;
    height: 100vh !important;
    display: flex;
    flex-direction: row;
  }
  .world .phone-side {
    height: 100vh !important;
    width: 100%;
    background: #eee;
    display: flex;
    justify-content: center !important;
    align-items: center !important;
  }
  .world .info-side {
    height: 100%;
    width: 100%;
    background: #ffffff;
    font-family: "Rubik" !important;
    display: flex;
    flex-direction: column;
  }
  .main-info {
    flex: 95%;
  }

  .info-side h2 {
    padding: 20px 80px;
  }
  .info-side-footer {
    flex: 5%;
    display: flex;
    height: 100%;
    font-size: 16px;
    flex: 5%;
    height: 100%;
    border-top: 1px dashed #333;
    color: black;
    align-items: center;
    justify-content: center;
  }
  .info-side-footer a {
    color: #333;
  }
  .iphone {
    position: relative;

    width: 280px;
    height: 540px;
    background: var(--iphonespacegray);
    border-radius: 35px;

    z-index: 99;
    outline: none;
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
    overflow: hidden;
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
    background: var(--iphonespacegray);
    border-bottom-left-radius: 10px;
    border-bottom-right-radius: 10px;
  }
  .iphone .notch .camera {
    height: 10px;
    width: 10px;
    border-radius: 50%;
    background: #3d3d3d;
    margin-top: -3px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .iphone .notch .camera .camera1 {
    height: 5px;
    width: 5px;
    border-radius: 50%;
    background: #505050;
  }
  .iphone .notch .mouthpiece {
    height: 5px;
    width: 50px;
    background: #3d3d3d;
    border-radius: 2px;
    margin-right: 10px;
    margin-top: -3px;
  }
  .iphone .silentswicth {
    position: absolute;
    top: 12%;
    right: 100%;
    width: 3px;
    height: 15px;
    background: var(--iphonespacegray);
    border-top-left-radius: 3px;
    border-bottom-left-radius: 3px;
  }
  .iphone .volume {
    position: absolute;
    top: 20%;
    right: 101.5%;
  }
  .iphone .volume .volup {
    position: inherit;
    width: 5px;
    height: 30px;
    background: var(--iphonespacegray);
    border-top-left-radius: 3px;
    border-bottom-left-radius: 3px;
    cursor: pointer;
  }
  .iphone .volume .voldown {
    position: inherit;
    width: 5px;
    height: 30px;
    background: var(--iphonespacegray);
    border-top-left-radius: 3px;
    border-bottom-left-radius: 3px;
    margin-top: 40px;
    cursor: pointer;
  }
  .iphone .powerbtn {
    position: absolute;
    top: 20%;
    left: 100%;
    width: 5px;
    height: 70px;
    background: var(--iphonespacegray);
    border-top-right-radius: 3px;
    border-bottom-right-radius: 3px;
    cursor: pointer;
  }
</style>
