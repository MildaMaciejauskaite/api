
## Description
- [X] My system let users to use giphy image library, search their favorite gifs, upload them to giphy and
     get random image from giphy api

## Entity definition
Actually object is very big, and a lot of data comes from API requests, contains multiple entities

api_key -> (string < 50)
limit -> (int < 100)
rating -> (string < 2 )
q (search input) -> (string < 300)
ids -> (string < 50)
source_image_url -> (string < 500)

## API definition
All methods require api_key, which is must 

GET //api.giphy.com/v1/gifs/trending? - gets gifs trending right now |-> error 500 -> internal server error from giphy

GET //api.giphy.com/v1/gifs/search?' - gets specific gifs, require api key, and what you are willing to search |-> error 500 -> internal server error from giphy

GET //api.giphy.com/v1/gifs/random?' - gets random gif |-> error 500 -> internal server error from giphy

POST //upload.giphy.com/v1/gifs? |- requires api key, and source video url ( can be etc. youtube) + 
//api.giphy.com/v1/gifs? |- requires api key and ^ method response ID, to get uploaded gif -> error 500 -> internal server error from giphy
|-> error 400 -> bad request for giphy, invalid json format

##authentication
OAuth  create a secure passage for your access, and it uses RSA encryption as part of its setup

## UI definition

 link to basic layout view: i will show
