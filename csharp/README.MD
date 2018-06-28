Advises for compiling the C# multiplatform project:
-When you load the solution, it contains 3 projects, one for each platform; you want to keep only the project for the platform you are working loaded, so you should unload the others because they won't compile anyway; so for example for Windows, right-click the OSX and GTK project and click 'Unload project'

-When you first compile the project it should restore the SciterSharp NuGeT package automatically; if for some reason compiling gives an error that SciterSharp was not found, it is because it was not properly restored; to solve it manually add the proper NuGeT package for the given project platform (SciterSharpWindows, SciterSharpOSX or SciterSharpGTK)

-Linux/MonoDevelop users: do not use MonoDevelop flatpak installation because it runs in a sandbox and Sciter won't find system dlls (debugging throws a DllNotFoundException); install MonoDevelop as said in its site

http://misoftware.com.br/Bootstrap/Download