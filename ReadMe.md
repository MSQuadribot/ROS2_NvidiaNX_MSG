# ROS2 Interface Package to ease the use of ROS2 on the Nvidia Nx

This package include custom messages in order to ease the use of ROS2 on the Nvidia Nx.

## What are the available messages?

There are currently two integrated messages:
    CanBus
    CarControl

The CanBus message is used to send CAN messages via ROS2.
It does not use a CAN bus, but instead it contain both the data and the id.
It was design to be send over a ROS2 topic and to be displayed by a Node.
The goal is to create a friendly interface for the user in order to understand what is sent by the bus can.

The CarControl is used to send the characteristic of the car through a ROS2 topic.
It support element such as speed, steering angle and brake.
The idea is to use the keyboard to control the car, converting the input to a CarControl message.

# What are the packages using the messages?

Currently only one package is using both messages:
The ROS2 canbot package.