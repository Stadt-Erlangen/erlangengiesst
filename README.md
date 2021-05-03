[![Netlify Status](https://api.netlify.com/api/v1/badges/08c96eab-42a0-45d4-9767-656b62b441bc/deploy-status)](https://app.netlify.com/sites/internetoftrees/deploys) ![Node.js CI](https://github.com/technologiestiftung/giessdenkiez-de/workflows/Node.js%20CI/badge.svg?branch=master)  ![love badge](https://img.shields.io/badge/build%20with-%E2%99%A5-red) ![citylab badge](https://img.shields.io/badge/@-CityLAB%20Berlin-blue)

# [![Logo of _Gieß den Kiez_](./docs/images/logo.svg)](https://www.giessdenkiez.de)

---

![Screenshot of _Gieß den Kiez_](./docs/images/screenshot.png)

## About [_Gieß den Kiez_](https://www.giessdenkiez.de)

The consequences of climate change, especially the dry and hot summers, are putting a strain on Berlin's ecosystem. Our urban trees are drying out and suffering long-term damage: In recent years, more and more trees have had to be cut down and their lifespan is declining. In the meantime, the population is regularly called upon to help, but largely uncoordinated. [_Gieß den Kiez_](https://www.giessdenkiez.de) is was made to change that and enable coordinated citizen* participation in the irrigation of urban trees. This project was made by the [Technologiestiftung Berlin](https://www.technologiestiftung-berlin.de/de/startseite/) and the [CityLAB Berlin](https://www.citylab-berlin.org/).

---

## Repositories

This project is composed of multiple repositories:

- [React frontend (this is here)](https://github.com/technologiestiftung/giessdenkiez-de)
- [vercel.com DB API](https://github.com/technologiestiftung/giessdenkiez-de-postgres-api)
- [vercel.com Auth0 API (currently only for username and user deletion)](https://github.com/technologiestiftung/tsb-trees-api-user-management)
- [AWS Fargate Service for DWD rain data and Mapbox API vector tiles](https://github.com/technologiestiftung/giessdenkiez-de-dwd-harvester) 

Find more information about our Backend in the [documentation](https://github.com/technologiestiftung/giessdenkiez-de/wiki/Backend---Overview).

---

## Frontend Documentation
- [Setup & Installation](https://github.com/technologiestiftung/giessdenkiez-de/wiki/Frontend-%E2%80%93-Installation-&-Setup)
- [Configuration files](https://github.com/technologiestiftung/giessdenkiez-de/wiki/Frontend-%E2%80%93-Configuration-files)
- [Code Structure](https://github.com/technologiestiftung/giessdenkiez-de/wiki/Frontend-%E2%80%94-Code-Structure)
- [Working With Data](https://github.com/technologiestiftung/giessdenkiez-de/wiki/Frontend-%E2%80%94-Working-With-Data)
- [How it works](https://github.com/technologiestiftung/giessdenkiez-de/wiki/Frontend-%E2%80%93-How-it-works)
- [Tesing & Code Quality](https://github.com/technologiestiftung/giessdenkiez-de/wiki/Frontend-%E2%80%93-Testing-&-Code-Quality)
- [Deploying on Netlify](https://github.com/technologiestiftung/giessdenkiez-de/wiki/Frontend-%E2%80%94-Deployment-with-Netlify)

---


## Demo Mode

The purpose of the demo mode (created if you set the env variable `BUILD_TARGET=DEMO`) is to run this application in the exhibition of the CityLAB Berlin. In this mode all requests to the api get mocked responses except for the get tree by id and get all trees. It uses the [msw (Mock Service Worker)](https://github.com/mswjs/msw) module underneath to handle API requests and does a module replacement for the [auth0-spa-js](https://github.com/auth0/auth0-spa-js) library wrapper with webpack.  


To start the DEMO mode run.

```bash
npm run demo
```
<!-- trigger deploy 2020-08-05 12:55:46 :rocket: -->