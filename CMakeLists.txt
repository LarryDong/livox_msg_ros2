cmake_minimum_required(VERSION 3.8)
project(livox_ros_driver2)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)
find_package(builtin_interfaces REQUIRED)  # 若消息里涉及 Header/Time/Duration

# 生成接口（在 ament_package() 之前）
rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/CustomPoint.msg"
  "msg/CustomMsg.msg"
  DEPENDENCIES std_msgs builtin_interfaces
)

# 导出运行时依赖（让下游和环境正确找到类型支持）
ament_export_dependencies(rosidl_default_runtime)
ament_package()
