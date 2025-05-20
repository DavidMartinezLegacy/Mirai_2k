# Mirai_2k
A VIO EGO_UAV solution with a cost of less than 2000 RMB
# Hardware：
* Platform
[xi35pro](https://oddityrc.com/collections/xi35pro?sort_by=manual&filter.p.tag=xi35pro)
* Onboard computer
[鲁班猫4](https://doc.embedfire.com/products/link/zh/latest/linux/ebf_lubancat.html)
* Intel-realsense-depth-camera:
[D435](https://www.intel.cn/content/www/cn/zh/products/sku/128255/intel-realsense-depth-camera-d435/specifications.html)
[D430](https://www.intel.cn/content/www/cn/zh/products/sku/98320/intel-realsense-depth-module-d430/specifications.html)
# Software
* terimal 1
wget http://fishros.com/install -O fishros && . fishros

sudo apt-get install ros-noetic-realsense2-*
sudo apt-get install ros-noetic-mavros
cd /opt/ros/noetic/lib/mavros
sudo ./install_geographiclib_datasets.sh

sudo apt-get install liblapack-dev libsuitesparse-dev libcxsparse3 libgflags-dev libgoogle-glog-dev libgtest-dev

sudo apt-get install ros-noetic-ddynamic-reconfigure

* terimal 2
git clone https://github.com/ZJU-FAST-Lab/Fast-Drone-250.git
cd Fast-Drone-250
unzip 3rd_party.zip 
cd glog
sudo sh autogen.sh
sudo chmod +x configure
./configure
make -j8
sudo make install

cd ..
cd ceres-solver-2.0.0rc1
mkdir build
cd build
cmake ..
sudo make -j8
sudo make install
