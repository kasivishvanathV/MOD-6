# CPP MODULE 6 :

# 6a :

# PROGRAM STATEMENT :
Write a CPP program to REVERSE the Singly Linked List using STL and Display the same.

# ALGORITHM :
1. Include the necessary header files (<iostream> and <stack>) and define the main function.
2. Create a singly linked list and insert elements using a simple class or struct to define the linked list 
node structure.
3. Use a stack (std::stack) to push all elements of the linked list, and then pop them to reverse the order.
4. Traverse the stack and print the elements in reversed order to display the reversed linked list.
5. End the program after displaying the reversed list.

# PROGRAM :
NAME : V.Kasivishvanath
REG NO : 212222040073
```
#include <iostream>
#include <forward_list>
using namespace std;
int main() 
{
 forward_list<int> sll = {10, 20, 40, 30, 70};
 cout << "List elements before performing reverse operation: ";
 
 for (const int& elem : sll)
 {
 cout << elem << " ";
 }
 cout << endl;
 sll.reverse();
 cout << "List elements after performing reverse operation: ";
 
 for (const int& elem : sll)
 {
 cout << elem << " ";
 }
 return 0;
}
```

# OUTPUT :
 ![image](https://github.com/user-attachments/assets/49df7797-0c45-46ac-ba6b-60572507f38d)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 6b :

# PROGRAM STATEMENT :
Write a CPP program to an INSERT an Element at LOCATION 1 in Doubly Linked List Using 
STL and Display the same.

# ALGORITHM :
1. Create an empty list named gqlist1 and declare variables for input.
2. Use a loop to read 5 integer elements from the user and insert them at the back of gqlist1.
3. Read an additional integer from the user and insert it at the front of the list using push_front()
4. Traverse the list using a range-based loop and print each element.
5. End the program after displaying the elements of the doubly linked list.

# PROGRAM :
```
#include <iostream>
#include <list>
using namespace std;
int main() 
{
 list<int> gqlist1;
 int input, elementToInsert;
 for (int i = 0; i < 5; ++i) 
 {
 cin >> input;
 gqlist1.push_back(input);
 }
 cin >> elementToInsert;
 
 gqlist1.push_front(elementToInsert);
 cout << "List: ";
 
 for (int value : gqlist1) 
 {
 cout << value << " ";
 }
 cout << endl;
 return 0;
}
```

# OUTPUT :
 ![image](https://github.com/user-attachments/assets/b60e4df7-b361-4261-83f3-9a872a43c122)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 6c :

# PROGRAM STATEMENT :
Write a CPP program to SEARCH an element from the Circularly Linked List and Display the 
same.

# ALGORITHM :
1. Define a class or struct to represent a node of the circularly linked list with pointers for data and 
next node.
2. Create a function to insert elements into the circularly linked list by linking the last node back to the 
head node.
3. Create a function to search for an element by traversing the list until the element is found or the list 
loops back to the head.
4. In the main function, call the search function and display whether the element is found or not.
5. End the program after displaying the result of the search operation.

# PROGRAM :
```
#include<iostream>
using namespace std;
class Node
{
 public:
 int data;
 Node *nextptr;
}*head,*tail,*newn,*temp;
void display()
{
 temp = head;
 do
 {
 cout<<"Data = "<<temp->data<<" ";
 temp = temp->nextptr;
 }
 while(temp->nextptr!=head);
 cout<<"Data = "<<temp->data<<" ";
 cout<<endl;
}
void createNode(int n)
{
 newn = new Node();
 newn->data = n;
 newn->nextptr = 0;
 
 if(head==0)
 {
 head = newn;
 tail = newn;
 }
 else
 {
 tail->nextptr = newn;
 tail = newn;
 tail->nextptr = head;
 }
}
void Search(int d1)
{
 temp = head;
 bool ans = 0;
 for(int i = 0;i<5;i++)
 {
 
 if(temp->data == d1)
 {
 ans = 1;
 break;
 }
 else
 {
 temp = temp->nextptr;
 }
 }
 if(ans == 1)
 {
 cout<<"Element "<<d1<<" Found";
 }
 else
 {
 cout<<"Element not Found";
 }
}
int main()
{
 int n;
 for(int i=0;i<5;i++)
 {
 cin>>n;
 createNode(n);
 }
 int d1;
 cin>>d1;
 display();
 Search(d1);
 
}
```

# OUTPUT :
 ![image](https://github.com/user-attachments/assets/77bd0fe1-42d7-4373-b6b8-c9c87e4b0343)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 6d :

# PROGRAM STATEMENT :
Write a C++ function int printList(Node *head) to print the polynomial expression in polynomial 
addition program using Linked list concept.

# ALGORITHM :
1. Define a Node struct with coefficient and exponent as data members and a pointer next to the next 
node.
2. Create the printList(Node *head) function to traverse the linked list and print the polynomial terms 
in the form coefficient * x^exponent.
3. For each node, print the coefficient and exponent, considering proper formatting between terms (e.g., 
plus signs between terms).
4. Traverse the list from the head to the end, printing each term in the correct order.
5. End the function once the entire polynomial expression is printed.

# PROGRAM :
```
int printList(Node *head)
{
 
 cout << "Linked List" << endl;
 
 while(head != NULL)
 {
 cout << " " << head->coeff <<"x" << "^" << head->power;
 head = head->next;
 }
 
 return 1;
}
```

# OUTPUT :
 ![image](https://github.com/user-attachments/assets/a09c1064-e78a-47df-8e4f-f026df9e11a5)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.
