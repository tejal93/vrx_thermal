# vrx_thermal
ros build : colcon build --merge-install

source  :source ./install/setup.bash

ros2 launch vrx_gz competition.launch.py world:=sydney_regatta
gz topic -l
