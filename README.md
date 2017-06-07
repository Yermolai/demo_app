### Deployment instructions
To deploy the application on Heroku you will need to: 
-
-
-

#### To configure S3 bucket (needed for image and video uploading)

- Get access keys from AWS and put them into the heroku config vars:  <br />
    `S3_ACCESS_KEY`   <br />
    `S3_SECRET_KEY`   <br />
    `S3_BUCKET`          (bucket name)    <br />
- Check your `/config/initializers/shrine.rb` file and make sure that there is proper `region` of your bucket set <br />
  (http://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region)

#### To configure connections with Twitter, Instagram, Facebook and LinkedIn

- Register the app on your dev accounts on each of these platforms
- Get the following 8 keys:
>Instagram: Client ID, Client Secret  <br />
>Twitter: Consumer Key (API Key),Consumer Secret (API Secret)  <br />
>Facebook: App ID, App Secret  <br />
>LinkedIn: Client ID, Client Secret  <br />
