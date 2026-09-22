---
title: "Swarm Rescue"
summary: "A drone-swarm rescue strategy for the Swarm-Rescue simulation competition."
date: 2024
links:
  - name: Code
    url: https://github.com/FelineAlloy/swarm-rescue
  - name: Leaderboard
    url: https://emmanuel-battesti.github.io/swarm-rescue-website/leaderboard_2024_25_fra/
---
Swarm-Rescue is a simulation competition in which a team of 10 drones has to explore an unknown map, find wounded people, and bring them to a rescue zone. Communication range is limited, and some maps add communication dead zones, GPS-denied areas and zones that disable a drone.

Each drone senses its surroundings through a 360° LIDAR, a semantic sensor, GPS, a compass and an odometer. Submissions are scored on the share of people rescued, the fraction of the map explored, the health of the drones, and the time remaining. The simulator is built on Pymunk and Arcade.

## Our approach

- State machine controller for high level decision making.
- PID controller for the drone’s motion.
- Segmentation of the map into a grid and Dijkstra's algorithm for pathfinding.

## Results

I was part of [team 14](https://emmanuel-battesti.github.io/swarm-rescue-website/leaderboard_2024_25_fra/). We were one of only 10 teams to make it to the final round!

{{< video "team14_MyMapIntermediate01_none_rd1.mp4" "Our algorithm on a simple map" >}}
