# weather-app
Fetching current weather from OpenWeather APIs, implement designing, state management, API integration

### APIs Used
[Open Weather APIs](https://openweathermap.org/)
> Open weather API is used For fetching the current time weather 

```bash 
1. Hover over to https://openweathermap.org/api
2. choose current weather data -> navigate to API doc: https://openweathermap.org/current
```
#### 1. Generate an API key 
> you can generate n number of API keys, for this project I generated a new API key named API_KEY 
![](2.PNG)

### API Info
* Method: `GET`
#### To call current weather data, this is how you make the an API call
* URL: `https://api.openweathermap.org/data/2.5/weather?q={CITY_NAME}&appid={API_KEY}`
or 
* URL2: `https://api.openweathermap.org/data/2.5/weather?lat={lat}&lon={lon}&appid={API key}`

![](1.PNG)
> Reference: https://openweathermap.org/current

#### Replacing the CITYNAME and APIKEY with my custom city and generated APIKEY 
https://api.openweathermap.org/data/2.5/weather?q=Mumbai&appid=fbe27d003759d3f42d9e8fad4e0080b7
> when we enter this URL on a search engine, it returns this JSON object 
![](3.PNG)

```bash 
{
"coord": {
"lon": 72.8479,
"lat": 19.0144
},
"weather": [
{
"id": 721,
"main": "Haze",
"description": "haze",
"icon": "50d"
}
],
"base": "stations",
"main": {
"temp": 297.14,
"feels_like": 297.16,
"temp_min": 297.09,
"temp_max": 297.14,
"pressure": 1012,
"humidity": 60
},
"visibility": 2200,
"wind": {
"speed": 2.06,
"deg": 80
},
"clouds": {
"all": 69
},
"dt": 1645328593,
"sys": {
"type": 1,
"id": 9052,
"country": "IN",
"sunrise": 1645320860,
"sunset": 1645362645
},
"timezone": 19800,
"id": 1275339,
"name": "Mumbai",
"cod": 200
}
```
### Libraries used
* `styled-components`
* `axios`
* `react-scripts`

> To install styled components and axios libraries type this command in terminal 
```bash 
npm install styled-components axios --save
```
> Hover over to package.json in your directory, to confirm whether these packages have been installed in your application
```bash 
{
  "name": "weather-app",
  "version": "0.1.0",
  "private": true,
  "dependencies": {
    "@testing-library/jest-dom": "^5.16.2",
    "@testing-library/react": "^12.1.3",
    "@testing-library/user-event": "^13.5.0",
    "axios": "^0.26.0",
    "react": "^17.0.2",
    "react-dom": "^17.0.2",
    "react-scripts": "5.0.0",
    "styled-components": "^5.3.3",
    "web-vitals": "^2.1.4"
  },
```
