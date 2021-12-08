# Data-Engineering API(2) Spotify Web API, Endpoints & Mmethods, Parameters

## Spotify Web API Overview
> The project will use Spotify's Web API to fetch information from multiple artists

### Spotify Web API
- Access [Spotify for Developer] (https://developer.spotify.com/documentation/web-api/)

    ![ss](Images/WebApi.png)

- Rate Limiting
  - Limit on incoming requests from Spotify, which provides API (does not respond to infinite requests)

### Data, Reference
> Let's see what kind of data we can get through the API.

- Go to Reference and take a look

    ![ss](Images/Capture.png)
    ![ss](DE_img/Capture2.png) 
    ![ss](DE_img/Capture3.png) 
    - You can import master information about the artist
    - There is a sample on the right side of what data can be imported
    - We have a lot of resources on the left, and among them, we will use the information on 'Artist's Top Tracks' a lot.

---

## Endpoints & Methods
> Let's look at the Endpoints and Methods required when requesting an API.

    ![ss](DE_img/screenshot67.png) 
    - You can check the method and endpoint by looking at the artist API information


### Resource
- Resource is information returned through API

- Multiple Endpoints exist in one Resource
  
  ![ss](DE_img/Capture4.png) 
  - There are several endpoints in the resource called 'Artists'

###
- Path/method to access Resource
- The value of the URL I want to retrieve/request data from, the path, where to make the request, point, point

### Method
- Actions allowed for resource (data) access (Get, POST, PUT, DELETE)

  ![ss](DE_img/Capture5.png) 

- Method definition
  
  ![ss](DE_img/Capture6.png) 
  - HEAD: Often used to check if the API works well

  ![ss](DE_img/Capture7.png) 
  - The 'GET' part is the method, and the latter part is the Endpoint


---

## parameters
> Options to be delivered together when making a request through the endpoint

### Parameter type

  ![ss](DE_img/Capture8.png) 
  ![ss](DE_img/Capture9.png) 
  ![ss](DE_img/Capture10.png) 
  - In the case of Artist, Authorization must be entered in the Header Parameter
  - Artist's id is entered in Path Parameters
  - You can also check Query Parameters by entering Top Tracks.

- example
    ```linux
    curl -X GET "https://api.spotify.com/v1/artists/43ZHCT0cAZBISjO8DG9PnE/top-tracks?country=SE" -H "Authorization: Bearer {your access token}"
    ```
    - The path parameter (Artist ID) is entered in the part after 'artists/' in the example
    - The country=SE part is the Query Parameter
    - The part marked with -H is the Header part, and Authorization is included in it.

