Libext library
Used in most Ufasoft C++ projects

Libext library has following main features:
	* unified classes for Win32/POSIX APIs
	* provides new C++11/14/17 classes for old compilers and STL implementations
	* provides lightweight implementation (comparing with the Boost library) of some utility classes


Latest Source Code:
https://github.com/ufasoft/libext

This repository on the GitHub actually is a wrapper around https://github.com/ufasoft/el repository, included as Git Submodule.
The only reason to do this is to provide multiple ways to use ufasoft/el library.

Someone can build and install it as a library. Then he should use standard  ./configure && make && make install in the ufasoft/libext.
Someone other can just include ufasoft/el as a subdirectory of his project and compile library's sources directly.






