                                       RPI system Architecture and documentation

---

### Flow of the application:
<img src="https://github.com/sakshi-seth-17/Centralized-Documentation/blob/main/SystemArchitecture.jpg" alt="Alt text" title="Optional title">

---
### Description of components

[IP Address tracker](https://github.com/TsailabBioinformatics/TrackIPAddress)
  - This component was created to overcome the issue of arbitary change of IP Address of RPIs. 
  - The script of this components runs indefinitely which makes sure that the most current IP address of the machine is stored in firebase making it easier to get lastest information without the need of connecting the machines to other hardware. 
  - This script is triggered and sends an email notification when the machine starts/restarts or when there is a change in the IP address. 


[Data Collector - RPI0](https://github.com/TsailabBioinformatics/Data-Collector-RPI0) 
   - If working with RPI0 refer this data collector script.
   - To make this script work both [Firebase API on webserver - RPI0](https://github.com/TsailabBioinformatics/RPI0-API) and [Database API on webserver](https://github.com/TsailabBioinformatics/SensorsData) service needs to be active. 
   - This component collects information from sensor and camera attached to the respective machine and stores it into firebase and database through a web API hosted on the webserver.


[Data Collector - RPI3](https://github.com/TsailabBioinformatics/Data-Collector-RPI3) \
   - If working with RPI3 refer this data collector script.
   - To make this script work [Database API on webserver](www.google.com) service needs to be active. 
   - This component collects information from sensor and camera attached to the respective machine and stores it into firebase and database through a Google API and web API hosted on the webserver respectively.

[Firebase API on webserver - RPI0](https://github.com/TsailabBioinformatics/RPI0-API) \
[Database API on webserver](https://github.com/TsailabBioinformatics/SensorsData) \
[Sensor Management](www.google.com) \
[Sensor Daily Report](www.google.com) 
