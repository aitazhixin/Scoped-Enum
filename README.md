# Scoped-Enum
There is a problem when using scoped enum in c++11 complied by g++4.8

When the code is compiled as: g++ -std=c++11 main.cpp senum.h -o main, there will throw errors:

senum.h:5:1: warning: elaborated-type-specifier for a scoped enum must not use the ‘class’ keyword [enabled by default]
 enum class MyCmd : uint16_t{
 ^
senum.h:5:12: error: use of enum ‘MyCmd’ without previous declaration
 enum class MyCmd : uint16_t{
            ^
senum.h:5:18: error: expected unqualified-id before ‘:’ token
 enum class MyCmd : uint16_t{

If the code is compiled as: g++ -std=c++11 main.cpp -o main, the error will not happen.


What is the reason?

