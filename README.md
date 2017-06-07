#### To configure S3 bucket (needed for image and video uploading)

- Get access keys from AWS and put them into the heroku config vars:

    `S3_ACCESS_KEY`   <br />
    `S3_SECRET_KEY`   <br />
    `S3_BUCKET`          (bucket name)
    
- Check your `/config/initializers/shrine.rb` file and make sure that there is proper `region` of your bucket set <br />
  (http://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region)


#### To configure connections with Twitter, Instagram, Facebook and LinkedIn

- Register the app on your developer accounts on each of these platforms and get the following 8 keys:

   |Platform  |Keys|
   |----------| --------|
   |Instagram|`Client ID`, `Client Secret`|
   |Twitter  |`Consumer Key (API Key)`, `Consumer Secret (API Secret)`|
   |Facebook |`App ID`, `App Secret` |
   |LinkedIn |`Client ID`, `Client Secret`|
   
- Put the keys into the code in the `.env` file and into the Heroku config vars. The names of the keys on Heroku should be the same as in the code: `FACEBOOK_KEY` and `FACEBOOK_SECRET`, `TWITTER_KEY` and `TWITTER_SECRET` and so on.

- Make sure that you have the needed urls set properly for the app on all four dev accounts. These urls are:

    1.`Website URL` - for example, https://yourfeed-site-staging.herokuapp.com <br />
    2.`Callback URL` or `Redirect URIs` - should have the form of _WEBSITE_URL/auth/PROVIDER_NAME/callback_, for example, https://yourfeed-site-staging.herokuapp.com/auth/instagram/callback
