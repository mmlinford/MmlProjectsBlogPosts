
# SWIFT Astrophysics Simulator on a fresh Debian 9.8 Installation
1. Install dependencies
   ```bash
   apt install git make autoconf libtool libhdf5-openmpi-dev libgsl-dev libfftw3-dev python-pip python-tk textlive texlive-latex-extra dvipng
   pip install h5py matplotlib
   ```
1. Get the project
   ```bash
   git clone https://github.com/swiftsim/swiftsim.git
   ```
1. Build the project
   ```bash
   cd swiftsim
   ./autogen.sh
   ./configure
   make
   ```
1. Run an example
   ```bash
   cd examples/HydroTests/SodShock_3D
   ./getGlass.sh
   python makeIC.py
   ../swift --hydro --threads=4 sodShock.yml
   python plotSolution.py 1
   ```
