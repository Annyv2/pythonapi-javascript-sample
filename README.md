# Python API and basic Javascript SPA
## Previous Steps

Create an API with Auth0's dashboard and add the scope `read:agenda` to it

## Python API instructions

### Running the example
In order to run the example you need to have `python` and `pip` installed.

You also need to set your Auth0 Domain and the API's audience as environment variables with the following names respectively: `AUTH0_DOMAIN` and `API_ID`, which is the audience of your API. You can find an example in the `.env` file.

```bash
# .env file
AUTH0_DOMAIN=example.auth0.com
API_ID=YOUR_API_AUDIENCE
```

Once you've set those 2 enviroment variables:

1. Install the needed dependencies with `pip install -r requirements.txt`
2. Start the server with `python server.py`
3. Try calling [http://localhost:3001/ping](http://localhost:3001/ping)

You can then try to do a GET to [http://localhost:3001/secured/ping](http://localhost:3001/secured/ping) which will throw an error if you don't send an access token signed with RS256 with the appropriate issuer and audience in the Authorization header. You can also try to  do a GET to [http://localhost:3001/secured/private/ping](http://localhost:3001/secured/private/ping) which will throw an error if you don't send an access token with the scope `read:agenda` signed with RS256 with the appropriate issuer and audience in the Authorization header.

## Javascript SPA instructions

Put the `client ID`, `domain` and `api audience` in the `auth0-variables.js` file and then serve the application using your preferred method. 
