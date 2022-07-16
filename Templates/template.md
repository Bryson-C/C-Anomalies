### Templates (Quirky Generics)
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

However some things just are a bit off. &nbsp;
  For example: In the function example templates are required to have an addition operator to work, but nothing is stopping you from using any other value &nbsp;

Contraints And Concepts[<sup>1</sup>](https://en.cppreference.com/w/cpp/language/constraints) can help this (Here is a good tutorial[<sup>2</sup>](https://www.cppstories.com/2021/concepts-intro/)) &nbsp;

### Concepts
```C++
// Say We Have A Print Function
template<typename T>
void print(T t)
{
  std::cout << t << "\n";
}

// This Works Fine Since Strings Can Be Handled By std::ostream Operator
print("Hello World!");

struct int3 {
	int x,y,z;
};
int3 arrayOfThree = (int3){.x = 1, .y = 2, .z = 3};
// This Gives An Error Because No ostream :(
print(arrayOfThree);

// If The `int3` Struct Looked Like This The Function Would Be Valid With `int3`'s
struct int3 {
	int x,y,z;
	friend std::ostream& operator<<(std::ostream& os, const int3& x);
};
std::ostream& operator<<(std::ostream& os, const int3&x)
{
	return os << "Int3: " << x.x << ", " << x.y << ", " << x.z << "\n";
}
// `print` Function Now Works For `int3`! :)

```
We Could Either Pray To A Higher Power Someone Implemented The std::ostream operator &nbsp

Alternitavely We Could
```C++

```

### Pack Parameters
> Ever Since C++17 My Life Has Been On A Downward Spiral
```C++
// Standard Template
template<typename... T>
// ...

// Pack Template
template<typename... T>
// ... 
```


### Resources
1. [Contraints And Concepts](https://en.cppreference.com/w/cpp/language/constraints)
2. [Here is a good tutorial](https://www.cppstories.com/2021/concepts-intro/)
