# IBM Functions Tests

## Python example with virtual environment

```
# access the folder
cd jokes

# install virutalenv local
pip install virtualenv 

# config and activate virtualenv
virtualenv virtualenv
source virtualenv/bin/activate

# install package in virtual environment
pip install pyjokes

# deactivate the virtual environment
deactivate

# zip files
zip -r jokes.zip virtualenv __main__.py

# deploy cloud function
ibmcloud fn action create jokes jokes.zip --kind python:3.7 --main joke
```

## Python example with docker

```
# access the folder
cd jokes

# docker build
docker build -t th1460/jokes .

# docker push
docker push th1460/jokes

# deploy cloud function
ibmcloud fn action create jokes --docker docker.io/th1460/jokes __main__.py --main joke
```

## References
https://cloud.ibm.com/docs/openwhisk?topic=openwhisk-prep
