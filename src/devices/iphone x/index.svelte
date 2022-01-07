<script>
  /*** IMPORT STATEMENTS ***/

  import Homescreen from "./homescreen.svelte";
  import Lockscreen from "./lockscreen.svelte";

  let screen = true;
</script>

<div class="iphone">
  <div class="screen">
    {#if screen}
      <Homescreen />
    {:else}
      <Lockscreen />
    {/if}
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
    transform: translate(-50%, -50%) scale(1.1);
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
