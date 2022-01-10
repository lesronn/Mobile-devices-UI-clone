<script>
  import Notificationarea from "./notificationarea.svelte";
  import IoIosSearch from 'svelte-icons/io/IoIosSearch.svelte'
  import IoIosMic from 'svelte-icons/io/IoIosMic.svelte'
</script>

<div class="searchscreen">
  <div class="search_container">
    <div class="search">
      <div class="icon"><IoIosSearch/></div>
      <input type="search" name="search" placeholder="Search" autocomplete="off">
      <div class="icon1"><IoIosMic/></div>
    </div>

    <div class="weather">
      <div class="weatherhead">
        <div class="left">
          <img src="/images/icons/weather.png" alt="" />
          <div class="wtitle">weather</div>
        </div>
        <div class="right">Show More</div>
      </div>
      <div class="weathername">Macho</div>
      <div class="weatherbody">
        Yo Lesron the man come class look sharp then come❗
      </div>
    </div>
  </div>
  
</div>

<style>
  .searchscreen {
    height: calc(100% - 30px);
    width: 100%;
    border-radius: 25px;
    /* backdrop-filter: blur(10px); */
    display: flex;
    
  }
  .searchscreen .search_container{
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    margin: 0px 7px;

  }
  .searchscreen .search_container .search{
    width:100%;
    height: 25px;
   display: flex;
   grid-template-columns: 10% 80% 10%;
   align-items: center;
border-radius: 5px;
    background: rgba(255, 255, 255, 0.3);
    /* padding: 0 5px; */
  }
  .searchscreen .search_container .search .icon{
    width: 17px;
    height: 17px;
    color: rgba(255, 255, 255, 0.5);
    flex: 10%;
  }
  .searchscreen .search_container .search .icon1{
    width: 20px;
    height: 20px;
    color: white;
    flex: 10%;
    
  }
  .searchscreen .search input{
   outline: none;
   border: none;
   background: none;
   color: #ffffff;
   flex: 80%;
  }
  input[type="search"]::-webkit-search-decoration,
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-results-button,
input[type="search"]::-webkit-search-results-decoration {
  -webkit-appearance:none;
}
 ::placeholder{
    color: rgba(255, 255, 255, 0.7);
  }

  .search_container .weather {
    background: rgba(255, 255, 255, 0.6);
    border-radius: 10px;
    margin-top: 25px;
    padding: 7px;
  }
  .search_container .weather .weatherhead {
    display: flex;
    width: 100%;
    justify-content: space-between;
  }
  .search_container .weather .weatherhead .right {
    font-size: 10px;
    mix-blend-mode: overlay;
  }
  .search_container .weather .weatherhead .left {
    text-transform: uppercase;
    display: flex;
  }
  .search_container .weather .weatherhead .left .wtitle {
    font-size: 10px;
    padding-left: 3px;
    mix-blend-mode: overlay;
  }
  .search_container .weather .weatherhead .left img {
    height: 13px;
    width: 13px;
    margin-right: 2px;
  }
  .search_container .weather .weathername {
    font-weight: bold;
    font-size: 9pt;
    padding-top: 5px;
  }
  .search_container .weather .weatherbody {
    font-size: 9pt;
  }
</style>
