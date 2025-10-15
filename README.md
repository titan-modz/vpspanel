
<h1 align="center">VPS PANEL</h1>
## Overview

## Installation
1. Clone the repository or download:
`git clone https://github.com/titan-modz/vpspanel`
`cd vpspanel`

2.Install Basics:
`apt update && apt install zip -y && unzip vps_panel_project.zip -d vps_panel_project`

3.Enter The Dictionary:
`cd vpspanel`

4. Build the Docker image:
`docker build -t vpspanel .`

5. Run the container:
`docker run -it -p 5000:5000 -v /var/run/docker.sock:/var/run/docker.sock vpspanel`

## License
(c) 2025 Azimee . This software is licensed under the MIT License.

