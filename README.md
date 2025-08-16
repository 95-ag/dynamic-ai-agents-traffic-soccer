# Traffic Navigation and Soccer AI

This project explores effective coordination strategies for multi-agent systems in two settings: traffic navigation (cars/drones) and soccer AI, leveraging heuristic control and supervised deep learning using data from Rocket League replays.

## About

We addressed coordinated actions in dynamic environments—first, developing robust collision avoidance and navigation strategies for cars and drones in Unity, then attempting to transfer real-world soccer play data into a simulated 2D soccer AI setting. Results highlight strong navigation performance and novel data-driven soccer strategies, with discussion of pitfalls and future directions.

## Experimental Setup

- Used the Unity engine for all simulations, with agents as cars and drones across open fields and intersections.
- Traffic navigation: Employed heuristic control (collision avoidance, incremental starts, PD controllers, A* path planning) and quadrant-based intersection management.
- Soccer AI: Collected over 2,000 Rocket League pro replays via the ballchasing API. Trained a deep feed-forward network on statistical features for 3v3 gameplay; evaluated performance and analyzed transfer challenges from 3D to 2D simulation.
- Compared both domains for emergent coordination, limitations, and possible improvements.

## Resources

- Full project report: [DD2438_A3_Dynamic_Interaction.pdf](./DD2438_A3_Dynamic_Interaction.pdf)
- Soccer AI dataset: Collected from Rocket League replays via [https://ballchasing.com/](https://ballchasing.com/)
- Sample Unity setup instructions for soccer model:  
  1. In `Packages/manifest.json` add: `"com.unity.barracuda": "2.0.0"`
  2. Place `model.onnx` in `Assets/Resources/`
  3. Run project in Unity

## References

- Van den Berg, J., Lin, M., & Manocha, D. (2008). "Reciprocal velocity obstacles for real-time multi-agent navigation."  
- Adler, F. P. (1956). "Missile guidance by three-dimensional proportional navigation."  
- Wu, W. et al. (2014). "Distributed mutual exclusion algorithms for intersection traffic control."  
- Kurach, K. et al. (2020). "Google Research Football: A Novel Reinforcement Learning Environment." AAAI.  
- Stone, P. et al. (2005). "Reinforcement Learning for RoboCup-Soccer Keepaway." Adaptive Behavior.  
- Hart, P. E., Nilsson, N. J., & Raphael, B. (1968). "A Formal Basis for the Heuristic Determination of Minimum Cost Paths."

## Acknowledgments

- Developed as part of **DD2438** at KTH Royal Institute of Technology.
- Contributors: Aishwarya Ganesan, Ernest Pokropek
- Forked from original repo: https://github.com/erno98/DD2438-Assignment3.git
