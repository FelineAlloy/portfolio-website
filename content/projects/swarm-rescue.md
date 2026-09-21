---
title: "Swarm Rescue"
summary: "A drone-swarm rescue strategy for the Swarm-Rescue simulation competition."
date: 2025-03-10 # TODO: replace with the date that fits
tags: ["Multi-Agent", "Robotics", "Python"]
links:
  - name: Code
    url: https://github.com/FelineAlloy/swarm-rescue
  - name: Leaderboard
    url: https://emmanuel-battesti.github.io/swarm-rescue-website/leaderboard_2024_25_fra/
---
Swarm-Rescue is a simulation competition in which a team of 10 drones has to explore an unknown map, find wounded people, and bring them to a rescue zone. Communication range is limited, and some maps add communication dead zones, GPS-denied areas and zones that disable a drone.

Each drone senses its surroundings through a 360° LIDAR, a semantic sensor, GPS, a compass and an odometer. Submissions are scored on the share of people rescued, the fraction of the map explored, the health of the drones, and the time remaining. The simulator is built on Pymunk and Arcade.

## My approach

TODO: describe the strategy: exploration, coordination between drones, handling the dead zones.

## Results

TODO: team name, ranking and score. The 2024-25 France leaderboard is linked above.
