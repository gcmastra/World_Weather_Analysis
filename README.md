# World_Weather_Analysis
## Student Name: Christopher Mastrangelo
Module 6 - created new repo and cloned it to local workstation 

The main body of the write-up for the Module 6 Challenge will go here.  The supplemental information below may be moved to its own file before I submit the assignnemnt. 

<hr>

## Additional Information to be included in the report - Technical Challenges
### Errors found in online course materials

Unit 6.2.4 - near the end the following piece of code is pasted into the API_practice notebook

"#" Create an endpoint URL for a city."<br>
city_url = url + "&q=" + "Bston"<br>
city_weather = requests.get(city_url)<br>
if city_weather.json():<br>
  print(f"City Weather found.")<br>
else:<br>
  print(f"City weather not found.")<br>
<br>
The lesson says this will result in city not found but it always returns TRUE because there is always a JSON response even if it contains the error code and messsage
<hr>
Unit 6.2.6 - the following statement (see image) of the course material is intended to show the difference if the blanks are not parsed/replaced out of the city name before
generating the URL.  However, the links for Cabo and Cabo+San+Lucas still do not work because the API Key is not valid.  So to do this comparison you would 
have to build the URL yourself in your notebook using your own API Key which is easy to do . . . 

![image](https://user-images.githubusercontent.com/86205000/127163664-fc99fc7e-468b-491d-bdae-6d8bb1f0ef0a.png)

This is part of the JSON response for "Cabo"<br>
<ul><li>coord: {
lon: -35.0333,
lat: -8.2833
}</li>
</ul>

Whereas THIS IS Cabo+San+Lucas<br>
<ul>
  <li>coord: {
lon: -109.9124,
lat: 22.8909
}</li></ul>

So this illustrates that Cabo and Cabo+San+Lucas are two different cities- Cabo alone brings up Cabo De Santo Augustinho in Brazil pop 208,000

### A few more observations

But what about cities that share the same name like wilmington or springfield- how would you distinguish between Wilmington MA and Wilmington NC  ? ?

What about "bluff" ? Same issue as Cabo? other examples: bluff, bend,  or college ? the word college appears in many city names 

Hilo in HI shows up in EVERY RUN because it is the closest city to almost ANY point in the Pacific Ocean

I still don't know why we couldn't take the top 25 cities from each country and then shuffle those to get real places people will go

I think it is mostly to teach people how the random functions work and the citipy module works

<hr>

Did a git push at the end of section 6.2.7

<hr>

Placeholder for the next error when I find it.

<hr>

### Some neat stuff I encountered along the way

First version of heat map in section 6.5.2 - the map "works" but something looks wrong.  What do you think? 
![image](https://user-images.githubusercontent.com/86205000/127306793-cff5c81a-b80f-4351-a36c-b5f417c86ca5.png)

The map displays properly but based on the data we gave it, New York city is "hotter" than Texas or Mexico City.  That doesn't seem right.

Seems unlikely but if you ask Google Maps to show "Resorts" in a search centered on a random place in New Caledonia, you get this . . 

![image](https://user-images.githubusercontent.com/86205000/127017078-20df8dce-0825-4dea-8c66-d0cc5bf09680.png)

Is there really a resort in New Zealand for $17 per night? LETS GO! But the airfare might wipe out that savings.

There are some really cool places in Greenland but is anyone really going to go there? 

![image](https://user-images.githubusercontent.com/86205000/127206910-a690c432-bded-4438-bf1c-4c746a49797d.png)

Just saying.  
