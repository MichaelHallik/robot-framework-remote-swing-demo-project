# robot-framework-remote-swing-demo-project

<b>Introduction:</b>

This is a demo test project, that uses the Robot Framework RemoteSwingLibrary, which is an external RF test library. See here for its project page: https://github.com/robotframework/remoteswinglibrary.

This demo project is actually just a simple POC that I did a couple of years ago. As such it is by no means representative of how a real-world test project should be set up and structured. For instance, there is code in the test cases and there is a function that contains merely one call to a lower-level function.

However, the goal for this project is to simply provide an example that will work out-of-the-box and that will show you by example how to technically get the RemoteSwingLibrary to work.

One further note: as you can gather from it's project pages, the RemoteSwingLibrary enables you to connect to a JVM running the Java Swing application, while running the RF itself with C-Python. Of course, you COULD also run the RF on Jython. However, in the latter case it would probably be better to simply use the SwingLibrary (https://github.com/robotframework/SwingLibrary). However, even when running on Jython, in certain cases you still might want to use the RemoteSwingLibrary, since the latter can be used to connect to a process running in a JVM on another (virtual) machine. Please see for details on when and how to use the Remote Library Interface (which the RemoteSwingLibrary utilizes): http://blog.xebia.com/the-robot-framework-remote-library-interface-using-the-remote-database-library-to-connect-to-ibm-db2/

<b>Project contents:</b>
The project consists of three folders:
- SUT: contains the software under test
- Test_libraries: contains the RemoteSwingLibrary and keyword documentation
- Test_code: consists the sample test cases as well as the test functions and other resources

<b>Assumes:</b>

1. A working Robot Framework (2.8.3 or later) installation.
2. Optionally: an editor atop the RF.
3. An installed Java JRE/JDK (1.6 or later).

<b>To run the demo:</b>

1. Download or clone the project.
2. Add the robot-framework-remote-swing-demo-project-master\\_Test_libraries\remoteswinglibrary-2.2.1.jar to the system variable PYTHONPATH. Create the system variable in case it does not yet exist. If you fail to take this step, the RemoteSwingLibrary can NOT be imported and it's keywords will not be found by the RF or your editor.
3. Open the file robot-framework-remote-swing-demo-project-master\\_Test_libraries\Test_code\Resources\ACTS_functions.txt in a text editor. In the *** Keywords *** section, change the first line of the 'Setup' keyword by replacing <your_path> with the path to the 'robot-framework-remote-swing-demo-project-master' folder as it exists on your file system. Save and close the text file.
3. Open the folder robot-framework-remote-swing-demo-project-master\\_Test_libraries\Test_code in your editor, select one or both of the test cases and run. For instance in RIDE (https://github.com/robotframework/RIDE): expande the two nodes 'Test design' -> 'Sample test cases', select one or both of the test cases and run. OR just run the robot-framework-remote-swing-demo-project-master\\_Test_libraries\Test_code\Sample_test_cases.txt directly with pybot (i.e. from a command line).
