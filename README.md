# ht-22.05

#include <iostream>
using namespace std;

class BASE 
{ 
public:
    int value1;
    int value2;
    //constructor 1
    BASE() 
    { 
        cout << "BASE constructor called." << endl;
    } 
    void AddBase() 
    {
        cout << "\n\tBASE: First value - ";
        cin >> value1;
        cout << "\tBASE: Second value - ";
        cin >> value2;
    }
    //destructor1
    ~BASE() 
    {
        cout << "BASE destructor called." << endl;
    }
};

class Child : public BASE 
{ 
public:
    int value3;
    int value4; 
    //constructor2
    Child()
    { 
        cout << "Child constructor called." << endl; 
    } 
    void AddChild()
    { 
        cout << "\n\tChild: First value - " ;
        cin >> value3;
        cout << "\tChild: Second value - ";
        cin >> value4;
    } 
    //destructor2
    ~Child() 
    { 
        cout << "Child destructor called." << endl;
    } 
};

class Child2 : public Child 
{ 
public: 
    int value5;
    int value6;
    //constructor3
    Child2()
    { 
        cout << "Child2 constructor called." << endl;
    } 
    void AddChild2()
    { 
        cout << "\n\tChild2: first value - ";
        cin >> value5;
        cout << "\tChild2: Second value - ";
        cin >> value6; 
        cout << endl;
    } 
    //destructor3
    ~Child2()
    { 
        cout << "Child2 destructor called." << endl;
    }
};

int main() 
{ 
    Child2 ch;
    ch.AddBase();
    ch.AddChild();
    ch.AddChild2();
    return 0;
}
