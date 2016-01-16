# Marathon Deployer

A simple script for deploying docker images to marathon-based cloud.

    docker run \
        -v /path/to/your/marathon.json:/marathon.json \
        -e MARATHON_URL=<your_marathon_url> avastsoftware/marathon-deployer

It will simply do the POST or PUT request to deploy your app.

What it does for you:

- construct the URL to deploy
- do PUT request to marathon with provided JSON file
- parse response and set the return code accordingly
