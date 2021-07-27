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

<hr>

Section 6.2.7 - this is a code discrepancy rather than a problem in the online course  materials per se. 
When I try to create a cities list longer than 450 members, my code will not run.  If maxsize >= 500 my list comes back with a zero length
Maybe I should use a try-catch method on this piece of code to see what happens?

![image](https://user-images.githubusercontent.com/86205000/127178478-bb4eff83-9fb6-4241-9fca-8b3fd6c948ac.png)

<hr>

Placeholder for the next error when I find it.

<hr>

### Some neat stuff I encountered along the way

Unit 6.1.4 Random numbers, latitude and longitude - these random GPS coords come up with some far out locations
![image](https://user-images.githubusercontent.com/86205000/127003929-74c23a71-ca41-4159-ad64-6e1b8f48070e.png)

Seems unlikely but if you ask Google Maps to show "Resorts" in a search centered on a random place in New Caledonia, you get this . . 

![image](https://user-images.githubusercontent.com/86205000/127017078-20df8dce-0825-4dea-8c66-d0cc5bf09680.png)

Just saying.  
