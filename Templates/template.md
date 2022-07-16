### Templates
> Templates Allow The C++ Compiler To Generate Code Acording To What Is Demanded

### Template Structure
```C++
// Class Template
template<typename T>
class SomeClass {
  T m_TemplateClassMember;
  //...
}

// Function Template
template<typename T>
T SomeFunction(T a, T b) 
{
  // assuming type T has a addition operator
  return a + b;
}
```
This is the basic template structure &nbsp;

However some things just are a bit off. For example: In the function example templates are required to have an addition operator to work,
but nothing is stopping you from using any other value &nbsp;

[Contraints And Concepts](https://en.cppreference.com/w/cpp/language/constraints) can help this ([Here is a good tutorial](https://www.cppstories.com/2021/concepts-intro/)) &nbsp;
