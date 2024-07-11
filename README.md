# EVerest Testing

[EVerest](https://everest.github.io) is an open-source software project designed to support and advance electric vehicle (EV) charging infrastructure. EVerest aims to provide a universal, scalable, and flexible software stack for EV charging stations. The goal is to standardize and simplify the development of EV charging solutions.  EVerest is part of [LF Energy](https://lfenergy.org/), a [Linux Foundation](https://www.linuxfoundation.org/) project dedicated to accelerating the energy transition through open-source software and collaborative development. The project is supported by a community of developers, companies, and organizations committed to advancing EV charging infrastructure.

EVerest is built with a **modular architecture**, allowing developers to customize and extend functionalities according to specific requirements. It ensures compatibility and **interoperability between different EV charging hardware and software**, which is crucial for widespread EV adoption. The project **adheres to global standards and protocols such as OCPP (Open Charge Point Protocol) and ISO 15118**, facilitating seamless integration with various EV charging networks.

EVerest comprises core components like the **Charge Point Management System (CPMS)**, which manages the overall operation of the charging station including user authentication, billing, and remote monitoring, and the Energy Management System (EMS), which optimizes energy consumption and load balancing for efficient and cost-effective operation. Additionally, **various plugins and extensions can be added to enhance the functionality of the charging stations**, such as support for renewable energy sources and grid integration.

EVerest is a significant initiative in the EV charging ecosystem, aiming to create a standardized, open-source solution that fosters innovation, reduces costs, and supports the global transition to electric mobility.  For an in-depth overview on how this all could work on an IoT device, please see this video from the [2024 Open EV Charging Summit](https://www.youtube.com/watch?v=yVRNRVuncAY).

To enjoy more EVerest hype, [watch Dr. Marco Möller of PIONIX GmbH more details and future plans](https://www.youtube.com/watch?v=zP6P5Q4xNEs).

## Benefits of EVerest

- **Open Source:**
    As an open-source project, EVerest encourages collaboration and innovation. It allows developers and companies to contribute to and benefit from a shared software stack.
- **Cost Efficiency:**
    By providing a ready-made, flexible software solution, EVerest reduces the development time and costs for companies looking to deploy EV charging infrastructure.
- **Scalability:**
    EVerest is designed to support a range of use cases, from small installations to large-scale charging networks, making it suitable for various deployment scenarios.
- **Sustainability:**
    The project promotes sustainable energy practices by enabling the integration of renewable energy sources and smart grid technologies into EV charging stations.

## Use Cases and Applications - [video](https://www.youtube.com/watch?v=OJ6kjHRPkyY)

- **Commercial Charging Networks:** Deployment in public and private charging networks to provide reliablegit and efficient charging services.
- **Residential Charging Solutions:** Integration with home energy management systems to optimize charging based on energy availability and cost.
- **Fleet Management:** Support for electric vehicle fleets by providing centralized management and control of charging operations.

## Pre-requisites

To run the EVerest, you should be on a [Mac](https://everest.github.io/nightly/tutorials/how_to_mac/index.html#tutorial-mac-main), Linux, or [WSL](https://learn.microsoft.com/en-us/windows/wsl/about).  However, the instructions here are more geared towards a Linux or WSL install.  Also, you will need to install the following tools.

- [Python](https://python.org) - Installed on Linux out of the box.
- [NodeJS](https://nodejs.org/en/) - We'll install diferent versions via [nvm](https://github.com/nvm-sh/nvm).
- [KeyTool](https://docs.oracle.com/en/java/javase/11/tools/keytool.html) - to install certificates for ISO 15118 communication.
- [Docker](https://www.docker.com/) - For containerization and external dependencies.
- [Direnv](https://direnv.net/) - Used to manage environment variables.

## Getting Started

### Install System Packages

```bash
sudo bash -c "apt update && sudo apt install -y git rsync wget cmake doxygen graphviz build-essential clang-tidy cppcheck openjdk-17-jdk docker docker-compose libboost-all-dev libssl-dev libsqlite3-dev clang-format curl rfkill libpcap-dev libevent-dev pkg-config libcap-dev"
```

### Install Python Packages

Execute the following in your terminal:



```bash
# Clone the latest EVerest Dev environment repo
git clone https://github.com/EVerest/everest-dev-environment
rm -rf everest-dev-environment/.git

# If the concept of venv is new to you, please read:
#   https://docs.python.org/3/library/venv.html
python -m venv venv
source venv/bin/activate
python -m pip install --upgrade pip setuptools wheel
pip install -r everest-dev-environment/dependency_manager/requirements.txt
```

### Install Node.js Packages

Execute the following within your terminal:

```bash
nvm use                  # To eliminate any issues, install/use the version listed in .nvmrc. 
npm i                    # install the packages needed for project
```

### Create the database

## Development

todo: test this by just installing the `edm` package via pip.

## Testing



