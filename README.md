<h1 align="center">Tripix</h1>
<p align="center">
  <img width="140" src="https://raw.githubusercontent.com/Malcom98/MOBILE_PICTURES-Tripix/master/TripixLogo.png?raw=true">
</p>
<hr>
This was a team project for Lumen Development (biggest programming competition in Croatia) of my teammate and me where I worked as a backend developer & database administrator.<br/>
Code is private because of security reasons. <br>
If anyone has a wish to see the code behind pictures shown below, please contact me via GitHub.
<hr/>
<h3 align="center">Technology Stack</h3>
<table>
  <tr>
    <td><img width="300" src="https://github.com/Malcom98/MOBILE_PICTURES-Tripix/blob/master/LogoLaravel.png?raw=true"></td>
    <td><img width="300" src="https://github.com/Malcom98/MOBILE_PICTURES-Tripix/blob/master/LogoMySql.gif?raw=true"></td>
    <td><img width="300" src="https://github.com/Malcom98/MOBILE_PICTURES-Tripix/blob/master/LogoReactNative.png?raw=true"></td>
  </tr>
</table>
<hr/>
<h3 align="center">Description</h3>
Tripix is iOS/Android travelling application that helps users to create travelling route. Tripix creates a new route with the shortest path between all attractions that were selected by user. It provides user with some usefull information like: travel time betwen two destinations, distance betwen two destinations, total distance, total duration etc.
User can:
<ul>
  <li>Create new route</li>
  <li>See his planned routes</li>
  <li>See his finished routes</li>
  <li>Generate 3 types of suggested routes by application</li>
  <li>See nearby cafes</li>
  <li>See nearby restaurants</li>
  <li>See nearby shops</li>
  <li>See nearby attractions</li>
</ul>
<br/>
<p align="center">
  <img src="https://github.com/Malcom98/MOBILE_PICTURES-Tripix/blob/master/TripixStartingScreen.png?raw=true"><br/>
  <b>Image 1 - Starting screen of an application</b>
</p>
<br/><br/>
<p align="center">
  <img src="https://github.com/Malcom98/MOBILE_PICTURES-Tripix/blob/master/TripixNewRoute_1.png?raw=true"><br/>
  <b>Image 2 - User creating new route part 1</b>
</p>
As mentioned earlier, user can create a new route by pressing "New Route" button on starting screen. User should enter route destination and pick planned route date. Application generates attractions ordered by highest rate and shows it to user.
<br/><br/><br/>
<p align="center">
  <img src="https://github.com/Malcom98/MOBILE_PICTURES-Tripix/blob/master/TripixNewRoute_2.png?raw=true"><br/>
  <b>Image 3 - User creating new route part 2</b>
</p>
User can also search attractions by name or select custom category to filter attractions. Available categories are: sports, pets, buildings, churchs, tourist attractions and parks.
<br/><br/><br/>
<p align="center">
  <img src="https://github.com/Malcom98/MOBILE_PICTURES-Tripix/blob/master/TripixNewRoute_3.png?raw=true"><br/>
  <b>Image 4 - User creating new route part 3</b>
</p>
User is able to see the best rated comment by holding finger for a second on wanted attraction. User is also able to see which attractions he/she selected for visiting. After that, user has to select trip starting point.
<br/><br/><br/>
<p align="center">
  <img src="https://github.com/Malcom98/MOBILE_PICTURES-Tripix/blob/master/TripixNewRoute_4.png?raw=true"><br/>
  <b>Image 5 - User creating new route part 4</b>
</p>
User has also to select trip ending point so the application can make shortest route of all attractions that user selected. After that, route overview is shown. Route overview gives user shortest path betwen all selected attractions. Route overview provides user with some useful information like: total trip time, total duration time, time betwen two destinations and distance betwen two destinations.
Application also shows user the shortest path on map.
<br/><br/><br/>
<hr/>
<h3 align="center">Back End API Endpoints</h3>
<b>/api/user</b>
<ul>
  <li>/login (POST) - Endpoint used for logging user.</li>
  <li>/register (POST) - Endpoint used for registering user.</li>
  <li>/stats (GET) - Endpoint used for getting user statistics.</li>
  <li>/verify (POST) - Endpoint used for verifying users account.</li>
  <li>/password/forgot (POST) - Endpoint used for sending forgotten password to users email.</li>
  <li>/password/code (POST) - Endpoint that is used when user enters forgotten password code.</li>
  <li>/password/new (POST) - Endpoint used creating new password.</li>
  <li>/change-email (POST) - Endpoint used to change users email. (when user logged in)</li>
  <li>/change-password (POST) - Endpoint used to change users password. (when user logged in)</li>
</ul>
<br/>
<b>/api/nearby</b>
<ul>
  <li>/restaurants (GET) - Endpoint used for getting nearby restaurants.</li>
  <li>/cafes (GET) - Endpoint used for getting nearby cafes.</li>
  <li>/shops (GET) - Endpoint used for getting nearby shops.</li>
  <li>/attractions (GET) - Endpoint used for getting nearby attractions.</li>
  <li>/cities (GET) - Endpoint used for getting nearby cities.</li>
</ul>
<br/>
<b>/api/photo</b>
<ul>
  <li>/{photo_reference} (GET) - Endpoint that gets photo based on photo reference.</li>
</ul>
<br/>
<b>/api/place</b>
<ul>
  <li>/{place_id} (GET) - Endpoint for getting best comment about place.</li>
</ul>
<br/>
<b>/api/attractions</b>
<ul>
  <li>/attractions/parks (GET) - Endpoint used for getting nearby park attractions.</li>
  <li>/attractions/stadiums (GET) - Endpoint used for getting nearby stadium attractions.</li>
  <li>/attractions/pets (GET) - Endpoint used for getting nearby pet attractions.</li>
  <li>/attractions/schools (GET) - Endpoint used for getting nearby school attractions.</li>
  <li>/attractions/religions (GET) - Endpoint used for getting nearby religion attractions.</li>
  <li>/attractions/landmarks (GET) - Endpoint used for getting nearby landmark attractions.</li>
</ul>
<br/>
<b>/api/route</b>
<ul>
  <li>/new (POST) - Endpoint for creating optimal route based on origin, destination and waypoints.</li>
  <li>/plan (POST) - Endpoint for saving route.</li>
  <li>/start (POST) - Endpoint for starting certain route.</li>
  <li>/finish (POST) - Endpoint for finishing certain route.</li>
  <li>/plan (POST) - Endpoint for saving route.</li>
  <li>/planned (GET) - Endpoint for getting planned routes.</li>
  <li>/started (GET) - Endpoint for getting started routes.</li>
  <li>/finished (GET) - Endpoint for getting finished routes.</li>
  <li>/suggested/{place} (GET) - Endpoint for getting suggested routes based on place passed in URL.</li>
  <li>/{id} (GET) - Endpoint for getting detailed information about route with id given in URL.</li>
</ul>
