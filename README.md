#### To configure connections with Twitter, Instagram, Facebook and LinkedIn

- Register the app on your developer accounts on each of these platforms and get the following 8 keys:

Instagram:`Client ID`, `Client Secret`
Twitter:  `Consumer Key (API Key)`, `Consumer Secret (API Secret)`
Facebook: `App ID`, `App Secret` 
LinkedIn: `Client ID`, `Client Secret`

- Put the keys into the code in the `.env` file and into the Heroku config vars. The names of the keys on Heroku should be the same as in the code: `FACEBOOK_KEY` and `FACEBOOK_SECRET`, `TWITTER_KEY` and `TWITTER_SECRET` and so on.

- Make sure that you have the needed urls set properly for the app on all four dev accounts. The main urls are:

`Website URL` - for example, `https://yourfeed-site-staging.herokuapp.com` 
`Callback URL` or `redirect URIs` - should have the form of `WEBSITE_URL/auth/PROVIDER_NAME/callback`, for example, `https://yourfeed-site-staging.herokuapp.com/auth/instagram/callback`
