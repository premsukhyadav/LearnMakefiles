# What is tutorial is about

This tutorial will help you to educate you with makefile. The approach the we
are going to use to learn it by doing it. we will build take small steps at a
time to learn things in great detail.

# Why to learn makefile
Anyone should learn makefiles to automate the build process for software project.
It defines a set of rules and dependencies that guide how files in your project
(like source code) should be compiled,linked, and organized into the final
executable or other desired outputs.

	#Analogy:
		Think of a Makefile as a recipe in a cookbook:

		The ingredients are your source files.
		The steps are the compilation and linking commands.
		The result is the final executable or program.
		
# Structure of a Makefile Rule
	target: dependencies
		command 
	
	#target: 
	The file to be created (e.g., an executable or an object file).
	Typically appears on the left side of the colon (:).
			
	#dependencies: 
	Files required to build the target. If any dependency changes,
	the commands are executed to update the target.
	
	#commands:
	Actions (e.g., compile or link) to build the target. Must be
	indented using a tab, not spaces.
	
