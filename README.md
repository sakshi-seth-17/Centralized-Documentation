                                       RPI system Architecture and documentation

---

### Flow of the application:
<img src="https://github.com/sakshi-seth-17/Centralized-Documentation/blob/main/SystemArchitecture.jpg" alt="Alt text" title="Optional title">

---
### Description of components

RPI
  - Necessary sensor and camera needs to be connected to the RPI before proceeding with further steps.

[IP Address tracker](https://github.com/TsailabBioinformatics/TrackIPAddress)
  - This component was created to overcome the issue of arbitary change of IP Address of RPIs. 
  - The script of this components runs indefinitely which makes sure that the most current IP address of the machine is stored in firebase making it easier to get lastest information without the need of connecting the machines to other hardwares. 
  - This script is triggered and it sends an email notification when the machine starts/restarts or when there is a change in the IP address. 


[Data Collector - RPI0](https://github.com/TsailabBioinformatics/Data-Collector-RPI0) 
   - If working with RPI0 refer this data collector script.
   - To make this script work both [Firebase API on webserver - RPI0](https://github.com/TsailabBioinformatics/RPI0-API) and [Database API on webserver](https://github.com/TsailabBioinformatics/SensorsData) service needs to be active. 
   - This component collects information from sensor and camera attached to the respective machine and stores it into firebase and database through a web API hosted on the webserver.


[Data Collector - RPI3](https://github.com/TsailabBioinformatics/Data-Collector-RPI3) 
   - If working with RPI3 refer this data collector script.
   - To make this script work [Database API on webserver](https://github.com/TsailabBioinformatics/SensorsData) service needs to be active. 
   - This component collects information from sensor and camera attached to the respective machine and stores it into firebase and database through a Google API and web API hosted on the webserver respectively.

[Firebase API on webserver - RPI0](https://github.com/TsailabBioinformatics/RPI0-API) 
   - RPI0 does not support firebase packages.
   - This API acts as a medium to store data on firebase.
   - The script in [Data Collector - RPI0](https://github.com/TsailabBioinformatics/Data-Collector-RPI0) sends the data to this API hosted on webserver and this API s uses Google API to store data to firebase.


[Database API on webserver](https://github.com/TsailabBioinformatics/SensorsData) 
   - This API acts as a medium to store data on SQLite database present on webserver.
   - The script in [Data Collector - RPI0](https://github.com/TsailabBioinformatics/Data-Collector-RPI0) and [Data Collector - RPI3](https://github.com/TsailabBioinformatics/Data-Collector-RPI3) sends the data to this API hosted on webserver to store it into the SQLite database


[Sensor Daily Report](https://github.com/TsailabBioinformatics/Reporting-Project)
   - This application is created to be able to monitor information collected from the sensor like temperature, humidity, brightness of the room and images on day to day basis.
   - The above information can be accessed for all the rooms where the machines are deployed.
   - The application can be accessed from [here](http://128.192.158.63:8501/).
   - If not in UGA's network, you will need a VPN to access this application.
   

[Sensor Management](https://github.com/TsailabBioinformatics/SensorManagementTool) 
   - This application is created to be able to monitor information collected from the sensor like temperature and humidity over last 7 days, image and current status of machines(active or inactive) of the room.
   - The application can be accessed from [here](http://aspendb.uga.edu/sensors).
   - If not in UGA's network, you will need a VPN to access this application.
