# Lattinone

Dear [Robot Programming]/[Probabilistic Robotics] student.
This is a virtual machine with supposedly everything you need to do exercises/projects related to your course.

Here you will find some useful informations to work with this system.
## Editors
We installed two main editors:

  - Visual Studio Code
  - Emacs

Feel free to install your favourite editor if you wish.

## Regarding ROS
**ros-noetic-desktop-full** is installed and you are provided with all the ROS functionality required for the exams and even more.
To enable ros functionalities you have to type in a terminal interface (shortcut ctrl-T):

     source /opt/ros/noetic/setup.bash

We integrated an alias in your bashrc file so that you can simply type `ws2` instead.

To compile C/C++ ROS projects, you require a specific workspace structure, please refer to the following [link](http://wiki.ros.org/catkin/Tutorials/create_a_workspace) for further instructions.
  `Note: the tutorials use 'catkin_make' to start the workspace compilation process. We use 'catkin build' which also allows for concurrent package compilation. You have to choose at the beginning which command you want to use, as the two are not compatibile with eachother. Please choose your favourite one and stick with it (use catkin build :D )`

     
    
  The directory which contains all the catkin workspaces is found at '/home/lattinone/catkin_ws/'.
  Here you will find the srrg2 workspace under the `catkin_ws/srrg2/` folder and your empty workspace at
  `catkin_ws/your_workspace`.
  If you wish to create a new workspace, follow these commands:

```sh
cd ~/catkin_ws
mkdir <your_workspace_name>
cd <your_workspace_name>
mkdir src
cd src
ws2
catkin_init_workspace
cd ../
catkin build
```
  Also remember that, to view in the ros environment the workspace's packages, you need to source the workspace itself.
  __After succesfully__ compiling the _<your_workspace_name>_ workspace, use:
```sh
source ~/catkin_ws/<your_workpace_name>/devel/setup.bash
```
Now you can use `rosrun <your_package_inside_your_workspace_name> <your_node>`
`REMEMBER` to compile your workspace, you must locate yourself at the root of the workspace folder first:
```sh
cd ~/catkin_ws/<your_workspace_name>
ws2
catkin build
```
       
## SRRG2 Suite 
You will find in `source/srrg2/` the set of our packages required by your project. Currently we have:
- srrg2\_config\_visualizer
- srrg2\_core
- srrg2\_executor
- srrg2\_laser\_slam\_2d
- srrg2\_qgl\_viewport
- srrg2\_slam\_interfaces
- srrg2\_solver
- srrg\_cmake\_modules
- srrg\_hbst

These packages are symlinked in the  `~/catkin_ws/srrg2/src/` folder to allow for workspace compilation.
### Including additional SRRG2 packages
`If you are required to add other packages, please refer to the "Contribute and Support" section and inform us using a GitHub Issue so that we will include it in the next release of Lattinone :)`
To include an additional package, do:
```sh
cd ~/source/srrg2
git clone <link_to_the_package_repo>
ln -s /home/lattinone/source/srrg2/<package_name> ~/catkin_ws/srrg2/src
```
    
## Contribute and Support
> It's your turn to contribute for Lattinone!
> Your colleagues and future students will be grateful

Here we would like to ask for your help.
If you:
- Think some relevant informations should be added to this README
- Spot a bug in the guide
- Spot a bug in Lattinone
- Have a suggestion/comply
- Have a question
- Want to hang out with us ;)

Please let us know by following this [link](https://github.com/EmanueleGiacomini/lattinone_readme/issues) and write an `Issue`
(Use some sense in the title as it will be the first thing we see)

## Useful Links
You may want to take a look at this material :)
| Cheatsheet | Link |
|-------|------|
|CMake | https://www.codewithharry.com/blogpost/cpp-cheatsheet/ |
|C++ | https://www.codewithharry.com/blogpost/cpp-cheatsheet/ |
|Octave | https://gist.github.com/obstschale/7320846 |
|ROS | https://w3.cs.jmu.edu/spragunr/CS354_S19/handouts/ROSCheatsheet.pdf |

Please remember to `havfun`
