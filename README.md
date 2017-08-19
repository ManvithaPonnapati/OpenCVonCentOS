# OpenCVonCentOS

Note to self to not fuck up things on ec2:

All the yum installs :

# groupsintall 'Development Tools':
bison - GNU Parser Generator) - used to develop language parsers. Ref: https://www.gnu.org/software/bison/  
byacc - yacc / ex <3 
cscope - vim - dev tool for c programming
ctags - indexing source and header files
cvs - concurrent versioning system
diffstat - diffstat reads the output of diff and displays a histogram of the insertions, deletions, and modifications per-file. It is useful for reviewing large, complex patch files.
doxygen 0 mainly intended as a documentation generation code for c++ - but i can use this for python and objC tooo.
flex - lexical analyser generator
gcc - 
gcc-c++
gcc-gfortran
gettext
indent
intltool
libtool
patch
patchutils
rcs
redhat-rpm-config
rpm-build
subversion
swig
systemtap
# other
pkgconfig
cmake 
tbb-devel - Intel’s Threading Building Blocks - make sure to enable this when you do the CMake.
eigen3-devel - NUMERICAL optimizations woooo!

# OpenCV - 3.3 is out
git clone https://github.com/Itseez/opencv_contrib.git
git clone https://github.com/opencv/opencv.git

create a build directory inside opencv folder 
cmake -D CMAKE_BUILD_TYPE=RELEASE \
    -D CMAKE_INSTALL_PREFIX=/usr/local \
    -D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib/modules \
    -D INSTALL_C_EXAMPLES=OFF \
    -D INSTALL_PYTHON_EXAMPLES=ON \
    -D BUILD_EXAMPLES=ON \
    -D BUILD_OPENCV_PYTHON2=ON ..

compile and isntall : make (this will take a while) , make install and ldconfig
