<script>
  import Notificationarea from "./notificationarea.svelte";
</script>

<div class="homescreen">
  <Notificationarea />
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
    height: 100%;
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
    margin: 10px;
    justify-content: center;
  }
  .homescreen .icons .row {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    margin-bottom: 20px;
  }
  .homescreen .icons img {
    height: 40px;
    width: 40px;
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
