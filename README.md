# GNU-Arm-Embedded-Toolchain-on-Ubuntu-20.04
Installation steps arm-none-eabi-gcc

##### Apply In Order for proper installation of the latest version 

ARM_TOOLCHAIN_VERSION=$(curl -s https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads | grep -Po '<h3>Version \K.+(?= <span)')

  curl -Lo gcc-arm-none-eabi.tar.bz2 "https://developer.arm.com/-/media/Files/downloads/gnu-rm/${ARM_TOOLCHAIN_VERSION}/gcc-arm-none-eabi-${ARM_TOOLCHAIN_VERSION}-x86_64-linux.tar.bz2"

sudo mkdir /opt/gcc-arm-none-eabi
  
sudo tar xf gcc-arm-none-eabi.tar.bz2 --strip-components=1 -C /opt/gcc-arm-none-eabi
  
echo 'export PATH=$PATH:/opt/gcc-arm-none-eabi/bin' | sudo tee -a /etc/profile.d/gcc-arm-none-eabi.sh
  
###### To make changes to take effect, logout and login to your system OR source /etc/profile
  
arm-none-eabi-gcc --version
arm-none-eabi-g++ --version  
  

#### SHOULD GİVE YOU --------->    
  /opt/gcc-arm-none-eabi/bin/arm-none-eabi-gcc

  
