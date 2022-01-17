<script>
  import Notificationarea from "./notificationarea.svelte";
  import IoIosSearch from "svelte-icons/io/IoIosSearch.svelte";
  import IoIosMic from "svelte-icons/io/IoIosMic.svelte";
  import IoIosMusicalNotes from "svelte-icons/io/IoIosMusicalNotes.svelte";
  import IoMdPhonePortrait from "svelte-icons/io/IoMdPhonePortrait.svelte";
  let currentime;
  const days = [
    "Sunday",
    "Monday",
    "Tuesday",
    "Wednesday",
    "Thursday",
    "Friday",
    "Saturday",
  ];

  const d = new Date();
  let day = days[d.getDay()];
  let date = d.getDate();
</script>

<div class="searchscreen">
  <div class="search_container">
    <div class="search">
      <div class="icon"><IoIosSearch /></div>
      <p>Search</p>
    </div>

    <div class="music">
      <img src="/images/misc.jpeg" alt="" />
      <div class="musictexts">
        <span>Now Playing</span>
        <b>Touch It</b>
        <span>KiDi</span>
      </div>
      <div class="icon"><IoIosMusicalNotes /></div>
    </div>

    <div class="eventsweather">
      <div class="event">
        <span class="etop">{day}</span>
        <span class="eday">{date}</span>

        <div class="edown">
          <p>No more</p>
          <span>events today</span>
        </div>
      </div>
      <div class="weather">
        <div class="wtop">
          <span>KT - Chambers...</span>
          <span>31°</span>
        </div>
        <div class="wdown">
          weather <br />

          <span>Thunderstorm </span>
          <br />
          <span>H:34°</span>
          <span>L:22°</span>
        </div>
      </div>
    </div>
    <div class="map">
      <div class="searchbtn">
        <IoIosSearch />
      </div>
    </div>
    <div class="siribattery">
      <div class="siri">
        <span>How to </span>

        <span>share it</span>

        <span>with siri</span>
      </div>

      <div class="battery">
        <div class="bcircle">
          <IoMdPhonePortrait />
        </div>
        <span class="percentage">80%</span>
      </div>
    </div>
  </div>
</div>

<style>
  .searchscreen {
    height: calc(100% - 30px);
    width: 100%;
    border-radius: 25px;
    backdrop-filter: blur(50px);
    display: flex;
  }
  .searchscreen .search_container {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    margin: 0px 15px;
  }
  .searchscreen .search_container .search {
    width: 100%;
    height: 27px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 7px;
    background: rgba(255, 255, 255, 0.3);
    cursor: not-allowed;
    /* padding: 0 5px; */
  }
  .searchscreen .search_container .search .icon {
    width: 17px;
    height: 17px;
    color: rgba(255, 255, 255, 0.5);
  }

  .searchscreen .search p {
    font-size: 14px;
    color: rgba(255, 255, 255, 0.5);
    padding-left: 5px;
  }
  .searchscreen .music {
    height: max-content;
    width: 100%;
    display: flex;
    background: rgba(255, 255, 255, 0.4);
    margin-top: 20px;
    border-radius: 15px;
  }

  .searchscreen .music img {
    width: 70px;
    height: 70px;
    margin: 10px;
    border-radius: 7px;
  }
  .searchscreen .music .musictexts {
    display: flex;
    flex-direction: column;
    height: 100%;
    justify-content: flex-end;
  }
  .searchscreen .music .musictexts span:first-child {
    font-size: 9px;
  }
  .searchscreen .music .musictexts span:last-child {
    font-size: 10px;
    padding-bottom: 10px;
  }
  .searchscreen .music .musictexts b {
    font-size: 11px;
    padding: 2px 0px;
  }
  .searchscreen .music .icon {
    width: 20px;
    height: 20px;
    margin-left: 55px;
    margin-top: 8px;
  }
  .searchscreen .eventsweather {
    width: 100%;
    display: flex;
    gap: 15px;
    justify-content: space-between;
    margin-top: 15px;
  }
  .searchscreen .eventsweather .event {
    background: #1c1c1e;
    width: 100%;
    padding: 8px;
    flex: 50%;
    display: flex;
    flex-direction: column;
    border-radius: 10px;
  }
  .searchscreen .eventsweather .event .etop {
    color: #ad2911;
    font-size: 10px;
    text-transform: uppercase;
  }
  .searchscreen .eventsweather .event .eday {
    font-size: 20px;
    color: white;
  }

  .searchscreen .eventsweather .event .edown {
    color: grey;
    font-size: 11px;
    margin-top: 10px;
  }
  .searchscreen .eventsweather .event .edown p {
    margin-bottom: 0px !important;
  }
  .searchscreen .eventsweather .weather {
    background: #3476b7;
    width: 100%;
    padding: 8px;
    flex: 50%;
    display: flex;
    flex-direction: column;
    border-radius: 10px;
    color: white;
  }
  .searchscreen .eventsweather .weather .wtop {
    display: flex;
    flex-direction: column;
  }
  .searchscreen .eventsweather .weather .wtop span:first-child {
    font-size: 10px;
    text-transform: capitalize;
  }
  .searchscreen .eventsweather .weather .wtop span:last-child {
    font-size: 30px;
    font-family: "sflight";
  }
  .searchscreen .eventsweather .weather .wdown {
    font-size: 9px;
  }
  .searchscreen .map {
    height: 90px !important;
    width: 100%;
    background: url("/images/map.png");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    margin-top: 20px;
    display: flex;
    align-items: flex-end;
    border-radius: 15px;
  }
  .searchscreen .map .searchbtn {
    height: 20px;
    width: 20px;
    padding: 3px;
    background: lightgrey;
    color: white;
    border-radius: 50%;
    margin-left: 10px;
    margin-bottom: 10px;
  }
  .searchscreen .siribattery {
    width: 100%;
    height: max-content;
    display: flex;
    gap: 15px;
    justify-content: space-between;
    margin-top: 15px;
  }
  .searchscreen .siribattery .siri {
    background: #febd00;
    width: 100%;
    height: 76px;
    padding: 10px;
    flex: 50%;
    display: flex;
    flex-direction: column;
    border-radius: 10px;
    font-size: 13px;
    justify-content: flex-end;
    font-weight: bold;
  }
  .searchscreen .siribattery .siri span:first-child {
    color: white;
  }
  .searchscreen .siribattery .siri span {
    color: yellow;
  }

  .searchscreen .siribattery .battery {
    background: rgba(255, 255, 255, 0.4);
    width: 100%;
    padding: 10px;
    flex: 50%;
    height: 76px;
    display: flex;
    flex-direction: column;

    border-radius: 10px;
  }
  .searchscreen .siribattery .battery .bcircle {
    height: 20px;
    width: 20px;
    padding: 5px;
    border-radius: 50%;
    border: 3px solid #febd00;
  }

  .searchscreen .siribattery .battery .percentage {
    margin-top: 10px;
    font-size: 30px;
  }
</style>
