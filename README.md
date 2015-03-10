# heroku-mms-agent

Why run yet another piece of your own infrastucture when you can make Heroku do it?

Easy:

1. Get your "Agent API Key" from MMS settings under *Administration > Group Settings*
and put it in monitoring-agent.config

2. Run the following command line incantations:

    ```sh
    heroku create --buildpack https://github.com/hone/heroku-buildpack-noop
    git push heroku master
    heroku ps:scale worker=1
    ```

3. There is no step 3.
