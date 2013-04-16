minsta
======

Minsta is a very simple web app for displaying all your instagram photos on a single page with sorting via filter.

Steps:

  1. Go to this URL and create an app: http://instagram.com/developer/clients/register/
  
  Enter in the URI of the your site. When you submit your form, you will get a client id and a client secret.
  Copy the client id somewhere as you will need it in a moment.

  Go this URL: https://instagram.com/oauth/authorize/?client_id=CLIENT-ID&redirect_uri=REDIRECT-URI&response_type=token
  
  Replace the CLIENT-ID and REDIRECT-URI with the client id you noted down and the URI you entered as the app URI. Hit enter
  and after you give authorization, you will be redirected to an address like this:

http://your-redirect-uri#access_token=####

You now have your access token.

Get your user id by going here: http://jelled.com/instagram/lookup-user-id

On line 57 of index.html:

url: "https://api.instagram.com/v1/users/############/media/recent/?access_token=##################",

Change the first set of hashes to your user ID. The second set is your access token.

That's it - you're good to go.
