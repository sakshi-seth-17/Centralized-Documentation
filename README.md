                                       RPI system Architecture and documentation

---

### Flow of the application:
<img src="https://github.com/sakshi-seth-17/Centralized-Documentation/blob/main/SystemArchitecture.jpg" alt="Alt text" title="Optional title">

---
### Description of components

[IP Address tracker]((https://github.com/TsailabBioinformatics/TrackIPAddress)) - This component was created to overcome the issue of arbitary change of IP Address of RPIs. The script of this components runs indefinitely which makes sure that the most current IP address of the machine is stored in firebase making it easier to get lastest information without the need of connecting the machines to other hardware. This script is triggered and sends an email notification when the machine starts/restarts or when there is a change in the IP address. \
[Data Collector - RPI0](www.google.com) \
[Data Collector - RPI3](www.google.com) \
[Firebase API on webserver - RPI0](www.google.com) \
[Database API on webserver](www.google.com) \
[Sensor Management](www.google.com) \
[Sensor Daily Report](www.google.com) 
