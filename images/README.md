# UML Diagrams

## Use Case
The use case diagram above represents the 5 main use cases of the system with its main actors. One of the main overall use cases of the system is to extract data from the system to make use by the actors. Different types of information can be extracted from the system including current alerts in the system and historic traffic data. 
## Domain Model
The main parts of the system include the intersections and vehicles. This is the primary source of the data and is where all the main interactions of the system will occur. 
## Class Diagram
The class diagram has 5 main classes TrafficManager, SystemState, Intersection, Transportation, and AlertSystem. These classes are responsible for a lot of the functionality withing the system. TrafficManager represents the overall system, it consumes data and produces actions based on the data. SystemState is responsible for collecting data from Intersections and Transportation. Intersection is responsible for controlling the traffic lights within the physical intersection itself along with collecting data about the intersection including traffic flow and weather. Transportation is responsible for collecting data from specific routes including buses and trains.  AlertSystem is responsible for generating alerts that are provided by TrafficManager. 
## Sequence Diagrams
The sequence diagrams represent the 5 main use cases for the system with its involved actors. While the main functionality of the system is to optimize traffic flow through the system by controlling traffic lights there is still direct interaction from actors. First is overriding control of the system because machine learning is in direct control of the different intersections, it is important that these controls can be overridden by a controller. Sequence diagrams 2-4 represent how drivers and first responders can view active alerts including weather, accidents, and traffic. The final sequence diagram represents the system returning historic traffic data that can then be used by a city planner to improve the system.  
## State Diagram
The state diagram represents the main functionality of the system. The main functionality includes collecting data and making decisions on that data to control traffic lights and sending out alerts based on the data collected. This cycle repeats itself if the system is running. 
## Activity Diagram
The activity diagram above shows the main use case of the system, collecting data and controlling traffic lights within the system.  
## Componenet Diagram
The component diagram above represents the overall system. The Traffic Controller contains most of the components within the system. It directly interfaces with intersections and vehicles to collect data for consumption. These interfaces can be extended beyond their current implementations to include more data from different sources. 
## Deployment Diagram
The diagram above represents a cloud deployment diagram utilizing AWS services. A blue green deployment pattern was chosen because there can be no downtime between releases. The system is critical and puts lives at risk if there is any downtime between releases. Along with cloud deployment embedded systems will be deployed to every intersection in the system. They are responsible for collecting the data at the intersections so that it can be sent to the cloud deployment for processing. Along with the EC2 instances an RDS instance is needed to store historical data. This data is not used in the main operation of the system so redundant storage is not needed.   
## Skelton Classes and Table Definitions
The data model represents historical data stored in the system. Each of the intersection state entries is time tagged with the time the data was collected. The ID on the intersection state table is the primary key and is used in other tables that store further information about the state at a given time. The skeleton classes show the main classes involved in the system along with their functions and attributes


