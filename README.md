# Sandpit

Steps to test the Weather API :

1) Import Sandpit\soapui-mock-app\MockWeatherWebService-soapui-project.xml to SOAP UI

2) Run both mock services 

    a)GlobalWeatherSoap12 MockService - Runs at port 8000 -  http://localhost:8000/mockGlobalWeatherSoap12?WSDL
    
    b)GlobalWeatherSoap MockService - Runs at port 8080  - http://localhost:8088/mockGlobalWeatherSoap?WSDL
    
3) Import Mule project to Anypoint Studio 

4) Deploy project using Run as Mule Application

5) API URLS 

    a) http://localhost:8081/data/v1/geo/Australia/cities  - Return cities for a country
    
    b) http://localhost:8081/data/v1/weather?country=Australia&city=Melbourne - Return weather for a country and a city combination
    
    c) http://localhost:8081/data/v1/geo  -  Return Country and country Code

6) Mule Config property file located at - /weather-api/src/main/resources/weather-api.properties

      http.port=8081
      wsdl.url.soap11=http://localhost:8088/mockGlobalWeatherSoap
      wsdl.url.soap12=http://localhost:8000/mockGlobalWeatherSoap12
