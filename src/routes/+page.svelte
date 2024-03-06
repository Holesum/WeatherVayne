<style>
  screen {
    /*layout*/
    display: grid;
    /*learn to use gridtemplate*/
    grid-template:
    "weather-card weather-card"
    "weather-card weather-card"
    "daily-weather-card hourly-weather-card"
    "daily-weather-card hourly-weather-card"
    "daily-weather-card hourly-weather-card"
    "input button"
    ;
    
    padding: 20 px;
    /*style*/
    background-color: rgb(205, 235, 235);
    font-family: 'Courier New', monospace;
    font-size: 36px;
    border: 1px solid gray;
    min-height: 100%;
    justify-items: stretch;
    align-content: space-evenly;
    column-gap: 5px; 
  }
  button {
    display: grid;
    padding: 20px;
    grid-area: button;
    background-color: navy;
    font-family: 'Courier New', monospace;
    font-size: 36px;
    border: 1px solid gray;
    min-height: 90%;
    justify-items: center;
    align-content: space-evenly;
  }
  weather-icon{
    min-width: 45px;
    min-height: 45px;
    max-height: 45px;
    max-width: 45px;
  }

  

  weather-card {
    display: grid;
    grid-template:
    "icon temp"
    "condition location";

    grid-area:weather-card;
    background-color: rgb(219, 218, 218);
    font-family: 'Garamond', Serif;
    border: solid 3px black;
    align-content: space-evenly;
    justify-content: space-evenly;
    min-height: 100%;
    font-size: 50px;
    margin-left: auto;
    margin-right: auto;
    min-width: 95%;
    justify-items: center;
    align-items: center;
  }

  daily-weather-card {
    display: grid;
    grid-template:
    "day1"
    "day2"
    "day3"
    "day4"
    "day5"
    "day6";

    background-color: rgb(219, 218, 218);
    grid-area:daily-weather-card;
    min-height:100%;
    border: solid 3px black;
    max-width: 100%;
    min-width: 100%;
    font-size: 25px;
  }

  day1{
    grid-area: day1;
    display: grid;
    grid-template:
    "icon day temp";
    align-content: center;
    align-items: center;
    justify-content: space-between;
    border: 2px solid black;
  }day2{
    grid-area: day2;
    display: grid;
    grid-template:
    "icon day temp";
    align-content: center;
    align-items: center;
    justify-content: space-between;
    border: 2px solid black;
  }day3{
    grid-area: day3;
    display: grid;
    grid-template:
    "icon day temp";
    align-content: center;
    align-items: center;
    justify-content: space-between;
    border: 2px solid black;
  }day4{
    grid-area: day4;
    display: grid;
    grid-template:
    "icon day temp";
    align-content: center;
    align-items: center;
    justify-content: space-between;
    border: 2px solid black;
  }day5{
    grid-area: day5;
    display: grid;
    grid-template:
    "icon day temp";
    align-content: center;
    align-items: center;
    justify-content: space-between;
    border: 2px solid black;
  }day6{
    grid-area: day6;
    display: grid;
    grid-template:
    "icon day temp";
    align-content: center;
    align-items: center;
    justify-content: space-between;
    border: 2px solid black;
  }
  daily-temp{
    grid-area:temp;
    justify-items: start;
    vertical-align: middle;
  } day {
    grid-area: day;
    justify-items: start;
    vertical-align: middle;
  } 

  hourly-weather-card {
    display: grid;
    grid-template:
    "hour1"
    "hour2"
    "hour3"
    "hour4"
    "hour5"
    "hour6";

    background-color: rgb(219, 218, 218);
    grid-area: hourly-weather-card;
    font-size: 25px;
    border: solid 3px black;
    min-width: 100%;
    max-width: 100%;
    align-content: stretch;
    align-items: stretch;
  }
  hour1{
    grid-area: hour1;
    display: grid;
    grid-template:
    "icon time-hour temp";
    align-content: center;
    align-items: center;
    border: 2px solid black;
  }hour2{
    grid-area: hour2;
    display: grid;
    grid-template:
    "icon time-hour temp";
    align-content: center;
    align-items: center;
    border: 2px solid black;
  }hour3{
    grid-area: hour3;
    display: grid;
    grid-template:
    "icon time-hour temp";
    align-content: center;
    align-items: center;
    border: 2px solid black;
  }hour4{
    grid-area: hour4;
    display: grid;
    grid-template:
    "icon time-hour temp";
    align-content: center;
    align-items: center;
    border: 2px solid black;
  }hour5{
    grid-area: hour5;
    display: grid;
    grid-template:
    "icon time-hour temp";
    align-content: center;
    align-items: center;
    border: 2px solid black;
  }hour6{
    grid-area: hour6;
    display: grid;
    grid-template:
    "icon time-hour temp";
    align-content: center;
    align-items: center;
    border: 2px solid black;
  }
  hourly-temp{
    grid-area:temp;
    justify-items: start;
    vertical-align: middle;

  } hour {
    grid-area:time-hour;
    justify-items: start;
    vertical-align: middle;

  }

  /*the different models for temperatures for each weather card*/
  temp { 
    grid-area: temp;
    justify-items: start;
    vertical-align: middle;
  }
  
  location {
    grid-area: location;
    font-size: 30px;
  }
  condition {
    grid-area: condition;
    font-size: 35px;
  }

  weather-day{
    grid-area: day;
  }

  weather-time{
    grid-area: time;
  }

  textInput {
    grid-area: input;
    min-width: 65%;
    font-size: 20px;
  }
</style>

<!--
<ion-card>  
  
</ion-card>
<popup>
  <button> click me </button>
  <ion-item class = "justify-content-center">
    <ion-img 
      src = "https://www.giantfreakinrobot.com/wp-content/uploads/2022/06/hellotherethumb.jpg"
      alt = " "
      style = "width:180%; background-color:pink; padding:5%;"
      class = "justify-content-center">
      
    </ion-img>
  </ion-item>
 
   {current_temp} 
  
    <ion-button shape = "round" 
      id ="foo1"
      color = "primary">
        yoda
    </ion-button>
  
   <ion-alert
    trigger = "foo1"
    header =  ""
    message = "hit a small child in my 2001 toyota corolla I did"
    ></ion-alert>
    <ion-button shape = "round" on:click={say_hello} aria-roledescription="button" href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">CLICK HERE FOR FREE VBUCKS</ion-button>
    </popup> 
-->
<screen>
  <weather-card>
    <temp>
      {convertTemp(currTemp).toFixed(0)}°
    </temp>
    <location>
      {cityName}, {currInitials}
    </location>
    <weather-icon>
      <ion-img 
      src = {decideIcon(currIcon)}
      alt = ""
      >
    </ion-img>
    </weather-icon>
    <condition>
      {currIcon}
    </condition>
  </weather-card>
  
  <daily-weather-card>
    <day1>
      <weather-icon>
        <ion-img 
      src = {decideIcon(dayIcon1)}
      alt = ""
      ></ion-img>
      </weather-icon>
      <daily-temp>
        {convertTemp(dayTemp1).toFixed(0)}°
      </daily-temp>
      <day>
      {decideDay(currentDay+1)}     
      </day>
    </day1>
    <day2>
      <weather-icon>
        <ion-img 
      src = {decideIcon(dayIcon2)}
      alt = ""
      ></ion-img>
        </weather-icon>
        <day>
          {decideDay(currentDay+2)}   
        </day>
        <daily-temp>
          {convertTemp(dayTemp2).toFixed(0)}°
        </daily-temp>
    </day2>
    <day3>
      <weather-icon>
        <ion-img 
          src = {decideIcon(dayIcon3)}
          alt = "">
        </ion-img>  
      </weather-icon>
        <day>
          {decideDay(currentDay+3)}     
        </day>
        <daily-temp>
          {convertTemp(dayTemp3).toFixed(0)}°
        </daily-temp>
    </day3>
    <day4>
      <weather-icon>
        <ion-img 
          src = {decideIcon(dayIcon4)}
          alt = "">
        </ion-img>
        </weather-icon>
        <day>
          {decideDay(currentDay+4)}    
        </day>
        <daily-temp>
          {convertTemp(dayTemp4).toFixed(0)}°
        </daily-temp>
    </day4>
    <day5>
      <weather-icon>
        <ion-img 
          src = {decideIcon(dayIcon5)}
          alt = "">
        </ion-img>
        </weather-icon>
        <day>
          {decideDay(currentDay+5)}    
        </day>
        <daily-temp>
          {convertTemp(dayTemp5).toFixed(0)}°
        </daily-temp>
    </day5>
    <day6>
      <weather-icon>
        <ion-img 
          src = {decideIcon(dayIcon6)}
          alt = "">
        </ion-img>
        </weather-icon>
        <day>
          {decideDay(currentDay+6)}     
        </day>
        <daily-temp>
          {convertTemp(dayTemp6).toFixed(0)}°
        </daily-temp>
    </day6>
  </daily-weather-card>
    
  <hourly-weather-card>
    <hour1>
      <weather-icon>
        <ion-img 
        src = {decideIcon(hourIcon1)}
        alt = "">
      </ion-img>
      </weather-icon>
      <hourly-temp>
        {convertTemp(hourTemp1).toFixed(0)}°
      </hourly-temp>
      <hour>
        {timeDecide(hour1)}:00{decideAM(hour1)}
      </hour>
    </hour1>
    <hour2>
      <weather-icon>
        <ion-img 
          src = {decideIcon(hourIcon2)}
          alt = "">
        </ion-img>
        </weather-icon>
        <hourly-temp>
          {convertTemp(hourTemp2).toFixed(0)}°
        </hourly-temp>
        <hour>
          {timeDecide(hour2)}:00{decideAM(hour2)}
        </hour>
    </hour2>
    <hour3>
      <weather-icon>
        <ion-img 
          src = {decideIcon(hourIcon3)}
          alt = "">
        </ion-img>
        </weather-icon>
        <hourly-temp>
          {convertTemp(hourTemp3).toFixed(0)}°
        </hourly-temp>
        <hour>
          {timeDecide(hour3)}:00{decideAM(hour3)}
        </hour>
    </hour3>
    <hour4>
      <weather-icon>
        <ion-img 
          src = {decideIcon(hourIcon4)}
          alt = "">
        </ion-img>
        </weather-icon>
        <hourly-temp>
          {convertTemp(hourTemp4).toFixed(0)}°
        </hourly-temp>
        <hour>
          {timeDecide(hour4)}:00{decideAM(hour4)}
        </hour>
    </hour4>
    <hour5>
      <weather-icon>
        <ion-img 
          src = {decideIcon(hourIcon5)}
          alt = "">
        </ion-img>
        </weather-icon>
        <hourly-temp>
          {convertTemp(hourTemp5).toFixed(0)}°
        </hourly-temp>
        <hour>
          {timeDecide(hour5)}:00{decideAM(hour5)}
        </hour>
    </hour5>
    <hour6>
      <weather-icon>
        <ion-img 
          src = {decideIcon(hourIcon6)}
          alt = "">
        </ion-img>
        </weather-icon>
        <hourly-temp>
          {convertTemp(hourTemp6).toFixed(0)}°
        </hourly-temp>
        <hour>
          {timeDecide(hour6)}:00{decideAM(hour6)}
        </hour>
    </hour6>
  </hourly-weather-card>
  <textInput>
    <input bind:value={inputCity} type="text" placeholder="insert city name here">
  </textInput>
  <button on:click={updateCity}>Update city</button>
  
</screen>

    <script>
      let lat = 0;
      let lon = 0;
      let currTemp = 0;
      let hourTemp1 = 0;
      let hourTemp2 = 0;
      let hourTemp3 = 0;
      let hourTemp4 = 0;
      let hourTemp5 = 0;
      let hourTemp6 = 0;
      let dayTemp1 = 0;
      let dayTemp2 = 0;
      let dayTemp3 = 0;
      let dayTemp4 = 0;
      let dayTemp5 = 0;
      let dayTemp6 = 0;
      let currIcon = '';
      let hourIcon1 = '';
      let hourIcon2 = '';
      let hourIcon3 = '';
      let hourIcon4 = '';
      let hourIcon5 = '';
      let hourIcon6 = '';
      let dayIcon1 = '';
      let dayIcon2 = '';
      let dayIcon3 = '';
      let dayIcon4 = '';
      let dayIcon5 = '';
      let dayIcon6 = '';
      
      let inputCity = ''
      let cityName = 'hempstead'
      let currState = '';
      let currInitials = '';

      // @ts-ignore
     // document.getElementById('updateCity').onclick = function() {
        // @ts-ignore
       // cityName = document.getElementById('cityInput').value;
      //}

      function updateCity() {
        cityName = inputCity;
        inputCity = '';
        loadPage();
      }

      let initials = function(/** @type {String} */ word){
        currInitials += Array.from(word)[0];
      }
      /**@param {string} city */
      async function getLatlong(city) {
        let url = 'http://api.openweathermap.org/geo/1.0/direct?q='+city+'&limit=1&appid=370d00d17c91e8c33160917c63efe5ed'
        const response = await fetch(url)
        const data = await response.json();
        lat = data[0].lat;
        lon = data[0].lon;
        currState = data[0].state;
        const stateArray = currState.split(" ");
        stateArray.forEach(initials);
        console.log(data)
      } 
      
      async function getWeather() {
        const response = await fetch('https://api.openweathermap.org/data/3.0/onecall?lat=' + lat + '&lon=' + lon + '&appid=370d00d17c91e8c33160917c63efe5ed')
        const data = await response.json();
        //getting the current temperature (in kelvin degrees)
        currTemp = data.current.temp;
        //getting the hourly temp for the next five hours (in kelvin degrees)
        hourTemp1 = data.hourly[2].temp;
        hourTemp2 = data.hourly[3].temp;
        hourTemp3 = data.hourly[4].temp;
        hourTemp4 = data.hourly[5].temp;
        hourTemp5 = data.hourly[6].temp;
        hourTemp6 = data.hourly[7].temp;
        //getting the daily temp for the next six days (in kelvin degrees)
        dayTemp1 = data.daily[2].temp.day;
        dayTemp2 = data.daily[3].temp.day;
        dayTemp3 = data.daily[4].temp.day;
        dayTemp4 = data.daily[5].temp.day;
        dayTemp5 = data.daily[6].temp.day;
        dayTemp6 = data.daily[7].temp.day;
        //poorly named: gets the current weather condition
        currIcon = data.current.weather[0].main;
        //poorly named: gets the hourly weather condition
        hourIcon1 = data.hourly[2].weather[0].main;
        hourIcon2 = data.hourly[3].weather[0].main;
        hourIcon3 = data.hourly[4].weather[0].main;
        hourIcon4 = data.hourly[5].weather[0].main;
        hourIcon5 = data.hourly[6].weather[0].main;
        hourIcon6 = data.hourly[7].weather[0].main;
        //poorly named: gets the daily weather condition
        dayIcon1 = data.daily[2].weather[0].main;
        dayIcon2 = data.daily[3].weather[0].main;
        dayIcon3 = data.daily[4].weather[0].main;
        dayIcon4 = data.daily[5].weather[0].main;
        dayIcon5 = data.daily[6].weather[0].main;
        dayIcon6 = data.daily[7].weather[0].main;

        console.log(data);
      }
      let convertTemp = function(/**@type {Number}*/ temp) {
        temp = (temp - 273.15) * 9/5 + 32
        return temp
      }
      
      async function loadPage() {
        currInitials = '';
        await getLatlong(cityName);
        await getWeather();
      }
      loadPage()
    

      //getting current date
      const now = new Date();
      let currentDay = now.getDay();
      const weekDays = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"];
      let decideDay = function(/** @type {Number} */ weekday) {
        if(weekday >= 7){
          weekday -= 7
        } return weekDays[weekday]
      }

      let current_time = now.getHours();
      let hour1 = current_time + 1
      let hour2 = current_time + 2
      let hour3 = current_time + 3
      let hour4 = current_time + 4
      let hour5 = current_time + 5
      let hour6 = current_time + 6
      if(current_time > 12) {current_time -= 12}
      let timeDecide = function(/**@type {Number}*/ time) {
        if(time > 24){
        time -= 24
      } else if (time > 12) {
        time -= 12
      } return time
      }
      let decideAM = function(/**@type {Number} */ time) {
        if(time > 12) {return "PM"} 
        else { return "AM"}
      }
      let decideIcon = function(/** @type {String} */ icon) {
        if(icon == "Rain"){
          return "/rainy.png"
        } else if(icon == "Clouds"){
          return "/cloudy.png"
        } else if(icon == "Clear"){
          return "/sun.png"
        } else if(icon == "Mist"){
          return "/Misty.png"
        } else if(icon == "Fog"){
          return "/foggy.png"
        }
      }

      
      
      //setInterval(update_temp, 1000)
    </script>
