# URL Shortener App
This is a simple URL shortener app built with Node.js, Express, MongoDB, Mongoose, nanoid on the backend and React and Typescript on the frontend.

## API
The app exposes one API endpoint:

*POST* https://cryptic-beach-13205.herokuapp.com/api/short - This endpoint accepts a JSON body with the key __originalUrl__ and its value being the long URL that you want to shorten. On success, it returns a JSON response that looks like this:
json
Copy code

`{
    "urlID": "1vhKFW3jZwd7Wu67P-cQg",
    "originalUrl": "https://www.google.com/search?q=fruits&sxsrf=AJOqlzVRhRrUkICTRO3cc12dWKshg9GAQQ:1677336757160&source=lnms&tbm=isch&sa=X&ved=2ahUKEwjezdCs9rD9AhWfWqQEHS0UC94Q_AUoAXoECAEQAw&biw=1366&bih=617&dpr=1#imgrc=Tx4xm7Li7U8gKM",
    "shortUrl": "https:/cryptic-beach-13205.herokuapp.com//1vhKFW3jZwd7Wu67P-cQg",
    "clicks": 0,
    "_id": "63fa211e8ba0c74479c01761",
    "__v": 0
}`


The **urlID** field is the unique identifier for the shortened URL, and the shortUrl field is the shortened URL that you can use to redirect to the original URL. 
The clicks field is the number of times the shortened URL has been clicked, and the _id field is the unique identifier of the document in the MongoDB database.

### Frontend
The frontend of the app was built with React and Typescript. When a user enters a long URL in the input field and clicks the "Submit" button, the app sends a POST request to the backend API to create a shortened URL. The app then displays the shortened URL on the page and allows the user to copy it to the clipboard.

When a user clicks on a shortened URL, the app sends a GET request to the backend API to get the original URL and then redirects the user to the original URL.

#### Deployment
##### Backend
The app is currently deployed on Heroku at https://cryptic-beach-13205.herokuapp.com/.
##### Frontend
