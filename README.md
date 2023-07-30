![Readme header image](https://i.imgur.com/KgHxGmA.jpg[/img][/img])


## :speech_balloon: Intro

This repository contains the work performed by our Team in application of the concepts learn at **Reinforcement Learning** course. The work performed here is not a RL exercise, but an integer programming problem. It has been solved using Pyomo library and it is an oversimplification of the problem that can be useful if you are starting to try integer programming or linear programming optimization problems. Basically, we will find the optimal production for a german restaurant offering just three products with a variable demand strongly dependent on weather temperatures.

## :rocket: How to use this repository

Here, you'll find just one notebook. All the data you need will be automatically included once running the notebook, as it is using the weather API of https://openweathermap.org/. It is worth mentioning that we are using Coincbc as solver. The installation of coincbc can be tricky, specially if you are running the code in Windows, and even more in Windows and Visual Studio. All the indications regarding coincbc can be found in their Github repository: https://github.com/coin-or/Cbc#download

## :package: Notebook introduction

The notebook is well explained and you will find an appropiate storytelling aligned with the code itself. In an oversimplification (and as a nod to our German friends) we have built a story around a restaurant from Munich that only sells three products which demand depends just on weather temperatures. The steps followed are the next ones:

- Capture the **weather data** since january 2021 until 7 days ago (no matter when you are running the code) using **OpenWeather API**
- Apply an **Autoarima model to get weather predictions for last 7 and next 7 days** (the model accuracy will vary according to the specific data that we have brought, but the objective that we have is not to build a really good forecast model as it is just for illustrating how the optimization can be applied)
- We stablish simple **demand functions for each product depending on the temperature.**
- We ask the user (in this case, the restaurant owner) to **insert a day**, that can be in the past or in the next 7 days looking at the future.
- For that day, we **retrieve the temperature for the day introduced**. Then we obtained the demand for each product.
- After having that, we **apply the optimization** itself, taking as objective function to maximize income and including demand and production constraints. We apply Coincbc as solver. **The restaurant owner will obtain the quantities that she has to produce, for each product, to get the maximum income.**

## :penguin: Authors

**Juan Francisco Horrillo** 
- Email : juan.horrillo@alumni.ie.edu
- Github : https://github.com/dianisley

**Alfonso Ferrándiz Hervella**
- Email : alfonsofhervella@alumni.ie.edu 
- Github : https://github.com/fonsofhervella

**Pedro Vicente Esteban Orellana**
- Email : pedrovesteban@alumni.ie.edu
- Github : https://github.com/callysthenes
