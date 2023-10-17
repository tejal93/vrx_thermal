# vrx_thermal
ros build : colcon build --merge-install

source  :source ./install/setup.bash

ros2 launch vrx_gz competition.launch.py world:=sydney_regatta
gz topic -l


# Thermal image gz topic :
/world/sydney_regatta/model/wamv/link/wamv/base_link/sensor/thermal_camera_sensor/image
gz topic -e -n 1 -t /world/sydney_regatta/model/wamv/link/wamv/base_link/sensor/thermal_camera_sensor/image

# Thermal image ros2 topic :
/wamv/sensors/Thermal_cameras/thermal_camera_sensor/image_raw
ros2 topic echo /wamv/sensors/Thermal_cameras/thermal_camera_sensor/image_raw
