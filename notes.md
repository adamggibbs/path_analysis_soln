#### mapping from path to tracker points
- first 120 points of path are "registration points." These can be used to help find transformation between path points and tracker points

#### transformation
- appears as if x and y coordinates got swapped from path to tracker
    - x_trk = -(y_pth)
        - relatively small error when assessed with mean absolute error between time series
    - y_trk = x_path ****with odd skew to it****
- appears as if the y_trk coordinates shift by a constant amount for a constant amount of time
    - for example, the coordinates are increased by 3 for 3 seconds, then decreased by 3 for the next 3 seconds (these numbers are completely arbitrary and are only used to show to pattern)
- tracker Z coordinates follow same repeating behavior as tracker Y

- path specifies no deviations from 0 for z coordinate, why does tracker have logs for movement along z axis?
    - perhaps this is inherent in the way the robotic arm moves?

- x_trk and y_path have the same amplitude
- y_trk and x_path have the same min and max values even though y_trk has the shifts described above

- seems like the robot might be getting held up when circles get completed, little kickbacks
- for each loop, the robot reaches corresponding points at the same time as the specified path. Suggests issue is in coordinate translation and not mechanics

- in 3D plot of the data, the specified path shape can almost be seen in the tracker path. 