# OAuth bridge template

This is a modification of mpj's OAuth bridge template intended for use with my single page react app Jammming (my codecademy intensive final project). This service logs in to Spotify and redirects the user to a given frontend application with a valid access_token as a parameter in the url. I modified this template by increasing the scope so that it could obtain the authorization required by Jammming.

## Runing Jammming Locally

In order to use this with Jammming, you have to simultaneously run this to act as a backend server to obtain authorization. It assumes that Jammming will be running on localhost:5000, but the server itself will be running on localhost:8888.

To run it locally, you must register the Spotify Application here:
https://developer.spotify.com/my-applications

On that page, add http://localhost:8888 as a callback url.

Write the below commands in your terminal (replacing XXXX AND YYYY with your acutal client id and secret from the page where you registered your application)

```
export SPOTIFY_CLIENT_ID=XXXX
export SPOTIFY_CLIENT_SECRET=YYYY
npm start
```

This will allow jammming to redirect you to the spotify login page to obtain authorization to modify and create playlists. 


