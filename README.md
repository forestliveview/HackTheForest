# HackTheForest
Setup
Server Environment setup

Flask-RESTful installation: pip install flask-restful
Dev version of flask-rest :
git clone https://github.com/flask-restful/flask-restful.git
cd flask-restful
python setup.py develop

Link: https://flask-restful.readthedocs.io/en/latest/installation.html#installation

After setup create file api.py with the following hello world sample
##################start


from flask import Flask
from flask_restful import Resource, Api

app = Flask(__name__)
api = Api(app)

class HelloWorld(Resource):
    def get(self):
        return {'hello': 'world'}

api.add_resource(HelloWorld, '/')

if __name__ == '__main__':
    app.run(debug=True)
    
    
##################end

run => python api.py

 * Running on http://127.0.0.1:5000/
 * Restarting with reloader
 
 on another cmd window test API using curl command
 curl http://127.0.0.1:5000/
 
 or in python console
 pip install requests
 import requests
 from requests import get
 get('http://localhost:5000/').json()
 
 .json() converts the data to json format
 
 using conda we installed packages for pylidar:
conda config --add channels conda-forge
conda config --add channels rios
conda create -n myenv pylidar
source activate myenv # omit 'source' on Windows

conda install -c conda-forge gdal
conda install -c conda-forge geos
