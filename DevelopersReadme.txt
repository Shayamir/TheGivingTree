Developers Readme for Tree.toe


v2 (10/4)
--
Highlights: 
  Switched from DAT to CHOP network. 
  Added Kinect support
LowLights:
  project1 is the main project's window
"Inputs" component contains manual, kinect and tree_hear_sensor inputs. switch1 toggles between kinect and manual modes
"Inputs Processor" component calculates the distance between person1 and person2 and assigns a color that represents this distance. Also, mesh_in and mesh_out are the placeholders for communicating with the learning system.
"Draw circles" component contains 6 instances of circle drawing corresponding to 6 persons

v1
--
In tree.toe you can find a container named: GivingTree which contains all the basis for the Giving Tree project

Two "Person" containers representing Kinect inputs are connected into a "Kinect_Data_Collector" Merge. 
X & Y coordinates are the only input collect for each person right now (may be extended if needed).
Another input component "Tree_Heart_Sensor" is fed along with "Kinect_Data_Collector" into "Inputs_Processor".
A "Debug_Null" container clones "Inputs_Processor" output.
The output of "Inputs_Processor" is fed into "Mapper" container which draws a circle per Person along with a color added by "Inputs_Processor".

"Inputs_Processor" module contains a "ColorUpdater" Python script that updates the color_table Table.
Another "Distances_Table" is being maintained but not used currently.
The Python scripts runs of every frame.
