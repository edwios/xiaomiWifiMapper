# WiFi heatmap generator

A Wi-Fi signal strength mapping tool using a Xiaomi Roborock S55 vacuum robot.
For details, see [![Aerodust](https://github.com/dgiese/aerodust)](https://github.com/dgiese/aerodust)

## Install

### Vacuum side

Upload the two python scripts inside run_on_vacuum to the vacuum robot
Execute `extract_pos` as a background process
E.g. `python3 extract_pos.py &`
When the vacuum cleaning starts, it will produce a `maps.csv` file in the same directory where `extract_pos.py` is located at.

## Use
Start vacuum cleaning.
When finished, copy over the maps.csv file to the computer.
Use any handy heatmap generator to process the maps.csv file to generate the required heatmap.

## Issues
If there is no Wi-Fi signal at all, the Wi-Fi connection on the robot will disconnect and `extract_pos.py` may block and not giving any output. This is until the Wi-Fi connection of the robot re-established.
