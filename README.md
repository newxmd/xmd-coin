## XMD COIN

### Website

* You can find everything about XMD at [xmdcoin.com](xmdcoin.com)


Compiling the coin :


Windows 64 bit (tested on windows 10 , windows 2016 server, windows 2008 server R2)

1.Download Microsoft Visual Studio Community Edition 2013 https://go.microsoft.com/fwlink/?LinkId=517284
2.Download latest cmake https://cmake.org/download/
3.Download Boost 1.5.7 MSVC 12.0 https://sourceforge.net/projects/boost/files/boost-binaries/1.57.0/boost_1_57_0-msvc-12.0-64.exe/download
4.Download Qt 5.8 (or latest) https://www.qt.io
5.Download Git for windows https://git-scm.com/downloads
6.Install all the above in the default locations (so next steps apply)
7.On your desktop create a folder "xmd"
8.inside this folder open a command line that has the git command in (for example a git bash, or a visual studio command line)
9.run "git clone https://github.com/upggr/xmd-coin.git xmd-coin"
10.Start cmake and point it to this folder for the source code and wherever you want the release binaries to be.
11.Define the following variables before clicking generate (Add Entry):
    a.QT5Core_DIR : C:/Qt/5.8/msvc2013_64/lib/cmake/Qt5Core
    b.QT5Gui_DIR : C:/Qt/5.8/msvc2013_64/lib/cmake/Qt5Gui
    c.QT5Widgets_DIR : C:/Qt/5.8/msvc2013_64/lib/cmake/Qt5Widgets
    d.BOOST_LIBRARYDIR : C:/local/boost_1_57_0/lib64-msvc-12.0
    e.BOOST_ROOT : C:/local/boost_1_57_0
12.Click configure
13.Click generate
14.Inside the folder you defined as the build folder on step 10 you will find a visual studio solutions file. Open it using visual studio
15.Make sure the project is set to Release in visual studio and select to RequestBuilder
16.The Binaries will be in the build folder after this finishes.


Compiling the wallet :

Windows 64 bit (tested on windows 10 , windows 2016 server, windows 2008 server R2)

1.Everything is per above steps, but you need to clone the wallet https://github.com/upggr/xmdwallet and inside this folder clone the coin https://github.com/upggr/xmd-coin.git
2.If you followed step 1 correctly using git or by downloading and unzipping from github, you should have a folder with the wallet source code and inside this folder a folder named xmd-coin that has the coin code.
3.As per above steps do the same as above from step 10 but using the wallet folder for all cmake operation.
4.You will end up with another visual studio solution file to compile
