# experiment-12

## AIM
To learn fucntion overloading in c++.

## Software Used
VS Code

## Problem Statement
1.) Write a c++ program to do function overloading.

2.) Write a c++ program to do operator overloading.

# Theory
### Function Overloading
Function overloading allows you to use the same function name for different tasks as long as the parameters (like types or numbers) are different. For example, you can have multiple print functions for integers, doubles, and strings. Just remember, the functions must have the same name but different parameters, and changing only the return type isn’t enough to distinguish them.

### Operator Overloading
Operator overloading lets you change how operators (like + or -) work with your own classes. This means you can define custom behavior for these operators without affecting their standard use. Most operators can be overloaded, but some cannot (like ::, ., and sizeof). Overloading operators makes your code easier to read and work with when using custom types.





## Problem Codes:
1:-
~~~ javascript
//Sharvari Murade
//23070123088
#include <iostream>
using namespace std;
int add(int a, int b) {
    return a + b;
}
float add(float a, float b) {
    return a + b;
}
int add(int a, int b, int c) {
    return a + b + c;
}
int main() {
cout << "Addition of 2 integers: " << add(7, 7) << endl;         
cout << "Addition of 2 floats: " << add(3.9f, 4.9f) << endl; 
cout << "Addition of 3 integers: " << add(7, 8, 9) << endl;      
return 0;
}
~~~

2:-
~~~ javascript
//Sharvari Murade
//23070123088
#include <iostream>
using namespace std;
class Complex {
    private:
    float real;
    float imag;
    public:
    Complex(float r = 0, float i = 0) {
        real = r;
        imag = i; 
    }
    Complex operator + (const Complex &obj) {
        Complex temp;
        temp.real = real + obj.real;
        temp.imag = imag + obj.imag;
        return temp;
    }
    void display() const {
        cout << real << " + " << imag << "i" << endl;
    }
};
int main() {
    Complex c1(3.5, 2.5);
    Complex c2(1.6, 3.7);
    Complex c3 = c1 + c2;
    cout << "First complex number: ";
    c1.display();
    cout << "Second complex number: ";
    c2.display();
    cout << "Sum of complex numbers: ";
    c3.display();
    return 0;
}
~~~

## Outputs
1:- 
<img width="294" alt="Screenshot 2024-09-15 at 8 43 38 PM" src="https://github.com/user-attachments/assets/6719ea07-cefd-4ea1-bbbb-a461fb1b4a86">

2:-
<img width="301" alt="Screenshot 2024-09-15 at 8 48 51 PM" src="https://github.com/user-attachments/assets/bc0e124c-1991-4d1a-903d-f7567d255680">

## Conclusion
In conclusion, function overloading enables you to use the same function name for different tasks by varying the parameters, while operator overloading allows you to customize the behavior of operators for your classes. Both techniques enhance code clarity and usability, making it easier to work with different types and maintain consistency in your programs.
