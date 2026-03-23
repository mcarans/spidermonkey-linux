# mozilla-2.0

Build:

    make -f libjs.make distclean
    make -f libjs.make -j16

Output of build in js/src/build-release

You can use distrobox to build for old gcc:

    distrobox create --name ubuntu22 --image ubuntu:22.04
    distrobox enter ubuntu22

Then:

    sudo apt update
    sudo apt install -y software-properties-common

    sudo add-apt-repository universe
    sudo apt update

    sudo apt install -y python2.7
    sudo apt install -y build-essential

    sudo apt install -y libnspr4
    sudo apt install -y libnspr4-dev

Then make:

    make -f libjs.make -j16
