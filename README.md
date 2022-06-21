# CS235-DataStructures-CppDemo


Please create a GitHub project with a file called CppDemo with the foillowing contents:

````
#include <iostream>
#include <fstream>  // (fstream stands for file stream)
#include <string>
#include <sstream>  // (sstream stands for string stream)
#include <list>

using namespace std;

int main(int argc, char *argv[]) {
////    How do you run the code?

    return 0;
}

````

You should remember how to compile your code.  If you do not please look over the previous class work to review.  Now that we have our environment all set up we will be able to review c++.  We will first learn what command line arguments are.  The following code will print all of the command line arguments given.=

````
////    What are command-line arguments?
    for (int i = 0; i < argc; ++i) {
        cout << argv[i] << endl;
    }
````

The next task we will learn how do you add the strings to a list?


````
////    void printList(list<string> myList) {
    for (auto it = myList.begin(); it != myList.end(); ++it) {
        cout << *it << endl;
    }
    cout << endl;
  }


////    How do you add the strings to a list?
    list<string> myList = list<string>();
    myList.emplace_back("First String");
    myList.emplace_back("Second String");
    myList.emplace_back("Third String");
    myList.emplace_back("Fourth String");
    myList.emplace_back("Fifth String");
    printList(myList);
````

Now try to sort your list of strings.

````
////    How do you sort the list?
    myList.sort();
    printList(myList);
````

How do you read strings from a text file?

````
////    How do you read strings from a text file?
    #include <fstream> // (fstream stands for file stream)
    ifstream inFileStream;
    inFileStream.open("items.txt");
    string line;
    if (inFileStream.is_open()) {
        while (getline(inFileStream, line)) {
            cout << line << endl ;
        }
    }
    inFileStream.close();
````

How do you write the list to a text file?

````
////    How do you write the list to a text file?
    ofstream outFileStream;
    outFileStream.open("items_out.txt");
    if (outFileStream.is_open()) {
        for (auto it = myList.begin(); it != myList.end(); ++it) {
            outFileStream << *it << endl;
        }
    }
    outFileStream.close();
````

 How do you convert from an int to a string?

````
////    How do you convert from an int to a string?
    int number = 4;
    stringstream ss = stringstream();
    ss << number;
    cout << ss.str();

    cout << to_string(number);
````

How do you convert from a string to an int?

````
////    How do you convert from a string to an int?
    cout << stoi("45") + stoi("45") << endl;
````


