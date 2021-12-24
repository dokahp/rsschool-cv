# Vitaliy Dreko

![Vitaliy Dreko logo](https://avatars.githubusercontent.com/u/13405257?v=4)

## Contacts

+ Location: Belarus, Minsk
+ Phone: +375(29) 363-07-08
+ email: vitali.dreko@gmail.com
+ github: https://github.com/dokahp


## About Me
Dreamer! Demanding of himself, but loyal to others. I like to study and I can call myself a greedy person when it comes to knowledge. I'm calm and patient person, but in critical moment I can stands up for myself. I chose the frontend, because I am a visual and I like that I can see the result of my work immediately. I will always continue study, to learn new things in order to achieve my main goal - to become a great professional!

## Skills
+ HTML5
+ CSS3
+ JavaScript
+ jQuery
+ Bootstrap
+ React (basics, learning now)
+ Git
+ VSCode

## Code Example

Side effect for functional component in React. Function returns a current weather forecast from dedicated api service "openweathermap"
```
useEffect(() => {
    function getCurrentWeather() {
      axios
        .get(
          `http://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${APIKEY}&units=metric`
        )
        .then((response) => {
          setCurrentWeather({
            temp: Math.round(response.data.main.temp),
            icon: response.data.weather[0].icon,
            description: response.data.weather[0].description,
          });
        });
    }
    // calls function for first time data
    getCurrentWeather();
    // calls every one minute to update data
    const interval = setInterval(() => {
      getCurrentWeather();
    }, 60000);
    return () => clearInterval(interval);
  }, [setCurrentWeather]);
```
