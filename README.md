# Weather App
This weather web app built with Flask and OpenWeather API displays the weather forecast for any city. I designed a simplistic UI to make it easier for the user to find the relevant information. All HTML, CSS, and Python code was written from scratch and the CSS is optimised for mobile and desktop through the use of CSS grid, flexbox, and media queries.

## Screenshots (Desktop)
<img src="/screenshots/weather_app_desktop_home_page_screenshot.png">
<img src="/screenshots/weather_app_desktop_forecast_page_screenshot.png">
<img src="/screenshots/weather_app_desktop_error_page_screenshot.png">

## Screenshots (Mobile)
<img src="/screenshots/weather_app_iphone_forecast_page_screenshot.png" style="width:400px;"> <img src="/screenshots/weather_app_iphone_home_page_screenshot.png" style="width:400px;">

## Reflection
Building a Python project from scratch without relying on a tutorial taught me a lot but I was also able to implement the app's key functionality (getting and displaying weather data) due to the work I did with APIs in Angela Yu's Python bootcamp. While deploying this web app, I  learned about git and version control as well as storing API keys as environment variables with .env and the purpose of .gitignore. This project turned out to be frustrating and complicated at times but I learned and grew a lot as a developer by tackling each problem. For instance, I struggled to make this website responsive because I discovered that the Chrome browser tools are not entirely accurate for the mobile view. Hence, when the app was deployed, the website didn't look the way I expected ore desired on mobile. So I switched to a free desktop application called Responsively and it provided views for multiple devices which allowed me to improve my CSS. In addition, I had difficulty positioning my footer at the bottom of my page and had to refer to [this resource](https://stackoverflow.com/questions/51683107/making-a-footer-stay-at-the-bottom-of-the-page-both-in-mobile-view-and-desktop-v) to adjust my CSS accordingly. 

If I were to do this project again, there are a few changes I would make. I would make the website render beautifully on iPads as well by eliminating the space between elements. I also wasn't sure how to add more functionality to this app while maintaining a seamless UI/UX design this time and I would love to do so in the future. E.g. I could add an option for users to specify the country of the city they enter (if multiple countries share the same city name). I could also display the low and high temperatures for each day in the five day forecast instead of only displaying the temperature at noon (which I understand is not an accurate estimate of the overall temperature). It would also be useful to enable location detection to allow the user to get more accurate weather data for their current location by using their precise coordinates instead of relying on the geocoding API provided by OpenWeather.  

## Useful Resources
- [OpenWeather API Documentation](https://openweathermap.org/api/one-call-3)
- [Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Guide to CSS Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [StackOverflow Post on Centering in CSS Grid](https://stackoverflow.com/questions/45536537/centering-in-css-grid)
- [Youtube video on searching blog posts with Flask](https://www.youtube.com/watch?v=kmtZTo-_gJY)
- [Article on retrieving HTML form data with Flask](https://www.geeksforgeeks.org/retrieving-html-from-data-using-flask/)
- [StackOverflow post on building Flask app search bar](https://stackoverflow.com/questions/39960942/flask-app-search-bar)
- [Article on storing API keys as environment variables](https://jonathansoma.com/lede/foundations-2019/classes/apis/keeping-api-keys-secret/)
– [StackOverflow post on storing API keys in Heroku](https://stackoverflow.com/questions/71593743/storing-api-key-in-heroku)
- [Making a footer stay at the bottom of the page both in mobile view and desktop view](https://stackoverflow.com/questions/51683107/making-a-footer-stay-at-the-bottom-of-the-page-both-in-mobile-view-and-desktop-v)

## Image Credit
- [Home page background image](https://unsplash.com/photos/2KXEb_8G5vo)
- [Error page desktop background image](https://unsplash.com/photos/U-Kty6HxcQc)

### Icons 
- <a target="_blank" href="https://icons8.com/icon/pLiaaoa41R9n/wind">Wind</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
- <a target="_blank" href="https://icons8.com/icon/37802/thermometer">Thermometer</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
- <a target="_blank" href="https://icons8.com/icon/99328/clouds">Clouds</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
- <a target="_blank" href="https://icons8.com/icon/101829/rain">Rain</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
- <a target="_blank" href="https://icons8.com/icon/67657/fog">Fog</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
- <a target="_blank" href="https://icons8.com/icon/hXkspV0LTEoE/snow">Snow</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
- <a target="_blank" href="https://icons8.com/icon/G3xS4dQTvswX/rainy-weather">Rainy Weather</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
- <a target="_blank" href="https://icons8.com/icon/101843/storm">Storm</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
- <a target="_blank" href="https://icons8.com/icon/59878/search">Search</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
- <a target="_blank" href="https://icons8.com/icon/39789/chevron-left">Chevron Left</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
- <a target="_blank" href="https://icons8.com/icon/99362/summer">Summer</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
- <a target="_blank" href="https://icons8.com/icon/akbaie9da2Be/tornado">Tornado</a> icon by <a target="_blank" href="https://icons8.com">Icons8</a>
---
###🌦 Python Weather App – Azure Deployment
🚀 Features

Search weather by city name

Uses Flask (Python) backend

Deployment with GitHub Actions → Azure App Service

Runs using Gunicorn in production

🛠️ Local Setup

Clone the repository:
```
git clone https://github.com/Devendrasaini1441/python-weather-app.git
cd python-weather-app
```
---
###Create & activate a virtual environment:
```
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

Install dependencies:
```
pip install -r requirements.txt
```

Create a .env file in the project root and add your API key:
```
OWM_API_KEY=your_openweather_api_key
```

Run locally (Flask development server):
```
flask run
```

App will run at: http://127.0.0.1:5000

##⚙️ Gunicorn (Production Server)

Azure App Service uses Gunicorn to run Flask apps in production.

Command used in deployment:
```
gunicorn --bind=0.0.0.0 --timeout 600 main:app
```

Here:

main → your Python file (main.py)

app → Flask application object

##🔑 Environment Variables on Azure

After deploying to Azure, go to:
Azure Portal → App Service → Configuration → Application Settings

Add:
```
OWM_API_KEY=your_openweather_api_key

```
Save & restart your app.

This is a Flask-based Python Weather App that fetches weather information using the OpenWeather API and is deployed to Azure App Service with GitHub Actions.

###☁️ Azure Deployment (With GitHub Actions)
##1. Create Azure Resources
```
Resource Group → weather-rg
```
App Service Plan → Linux

App Service (Web App) → python-weather-devendra

##2. Get Publish Profile

In Azure Portal → App Service → Get Publish Profile
```
Download the .PublishSettings file
```
##3. Add Secret in GitHub

Go to GitHub Repo → Settings → Secrets → Actions → New Secret
```
Name: AZURE_WEBAPP_PUBLISH_PROFILE
```
Value: Paste contents of .PublishSettings file

##4. GitHub Actions Workflow

Inside .github/workflows/azure-webapp.yml:
```
name: Deploy Weather App to Azure

on:
  push:
    branches:
      - main

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Set up Python
      uses: actions/setup-python@v2
      with:
        python-version: '3.9'

    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt

    - name: Zip artifact for deployment
      run: zip -r release.zip ./*

    - name: Deploy to Azure Web App
      uses: azure/webapps-deploy@v3
      with:
        app-name: "python-weather-devendra"   # your App Service name
        publish-profile: ${{ secrets.AZURE_WEBAPP_PUBLISH_PROFILE }}
        package: release.zip

```
---
###🌐 App URL

Once deployed, access your app at:
👉 https://python-weather-devendra.centralindia.azurewebsites.net

✅ Troubleshooting

500 Internal Server Error → Check logs:
```
az webapp log tail --name python-weather-devendra --resource-group weather-rg
```

Ensure OWM_API_KEY is added under App Settings in Azure Portal.

Check that your main.py has:
```
if __name__ == "__main__":
    app.run()
```

✨ Now your deployment is automated with GitHub Actions and runs on Gunicorn in Azure.
