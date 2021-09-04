AndroidAnalysisGUI

This is a guide to get the alpha release of Android Analysis GUI. It has only been tested on Linux.

1. Install Qt SDK.
	(1)Download the QtSDK (Qt_SDK_Lin32_offline_v1_1_1_en.run from "http://qt.nokia.com/downloads/sdk-linux-x11-32bit-cpp-offline") and install it using root permission.
	(2)Configure the environment variable.
	Add these to the end of the /etc/profile:
	
		QTDIR=/opt/QtSDK/Desktop/Qt/473/gcc
		PATH=$QTDIR/bin:$PATH
		LD_LIBRARY_PATH=$QTDIR/lib:$LD_LIBRARY_PATH
		export QTDIR PATH LD_LIBRARY_PATH

	Then save and exit:

	Execute the “source /etc/profile” , and “sudo updatedb” at last.

	If you can execute the “qmake –v” and can look at the version information, the Qt is installed successfully. 



2. Install SIP.
       (sip-4.12.3.tar.gz from "http://www.riverbankcomputing.co.uk/software/sip/download")

	(1)Firstly, you should install the python-dev, or there’are errors when executing “make”.
	(2)python configure.py
	(3)make
	(4)make install 


3. Install PyQt4
	(PyQt-x11-gpl-4.8.4.tar.gz from "http://www.riverbankcomputing.co.uk/software/pyqt/download")

	(1)tar xvfz PyQt-x11-gpl-4.8.4.tar.gz
	(2)python configure.py -g (then select "yes")
	(3)make
	(4)make install


4. Install pydot
       (pydot-1.0.25.tar.gz from "http://code.google.com/p/pydot/downloads/list")
	
	(1) python setup.py install


5. Install Graphviz
	(graphviz-2.28.0.tar.gz from "http://www.graphviz.org/Download..php")

	(1) ./configure --with-ortho=yes
	(2) make
	(3) make install

6. Install apktool
	(http://code.google.com/p/android-apktool/)

	# Linux:
   	(1). Download apktool-install-linux-* file
   	(2). Download apktool-* file
   	(3). Unpack both to /usr/local/bin directory (you must have root permissions) 


7. Run this tool:

	python startQT.py


[Others]: if you miss python lib dependency, you should install with the following two steps:
	(1) sudo apt-get install ipython
	(2) sudo apt-get install python-scipy
