# Instalación del Turtlebot2 en ROS melodic(Ubuntu 18.04)

## Creamos el espacio de trabajo

```
mkdir -p ~/turtlebot2_ws/src
cd turtlebot2_ws
catkin_make
```

```
cd src
curl -sLf https://raw.githubusercontent.com/gaunthan/Turtlebot2-On-Melodic/master/install_all.sh | bash
cd ..
catkin_make
```

```
echo "source ~/turtlebot2_ws/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

## Instalaciones de paquetes adicionales

```
sudo apt-get install ros-melodic-move-base*
```

```
sudo apt-get install ros-melodic-map-server*
```

```
sudo apt-get install ros-melodic-amcl*
```

```
sudo apt-get install ros-melodic-navigation*
```

## Finalmente se realiza la prueba de instalación

```
roslaunch turtlebot_stage turtlebot_in_stage.launch
```
