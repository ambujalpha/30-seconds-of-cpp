# priority_queue

**Description :** Priority queues are a type of container, specifically designed such that its first element is always the greatest of the elements.After deleting or inserting into the queue the queue rearranges itself to have the greatest element at the start.There is no ordering among the other elements only the first element is the largest ( hence different from reverse sorting as this is faster in case of upadating and finding largest).
**For Min Priority Queue**

#include <iostream> 
#include <queue> 
  
using namespace std; 
  
void showpq(priority_queue <int, vector<int>, greater<int>> gq) 
{ 
    priority_queue <int, vector<int>, greater<int>> g = gq; 
    while (!g.empty()) 
    { 
        cout << '\t' << g.top(); 
        g.pop(); 
    } 
    cout << '\n'; 
} 
  
int main () 
{ 
    priority_queue <int, vector<int>, greater<int>> gquiz; 
    gquiz.push(10); 
    gquiz.push(30); 
    gquiz.push(20); 
    gquiz.push(5); 
    gquiz.push(1); 
  
    cout << "The priority queue gquiz is : "; 
    showpq(gquiz); 
  
    cout << "\ngquiz.size() : " << gquiz.size(); 
    cout << "\ngquiz.top() : " << gquiz.top(); 
  
  
    cout << "\ngquiz.pop() : "; 
    gquiz.pop(); 
    showpq(gquiz); 
  
    return 0; 
}

Output - The priority queue gquiz is :     1    5    10    20    30

gquiz.size() : 5
gquiz.top() : 1
gquiz.pop() :     5    10    20    30

**Example** :

``` cpp

#include <iostream>
#include <array>
#include <queue>
#include <vector>
#include <functional>

int main ()
{
  std::array<int, 4> myints = {10, 60, 50, 20};
  std::vector<int> arr =  {1, 2, 3, 4};
  
  //empty queue
  std::priority_queue<int> first;
  
  //queue creation using array as input
  std::priority_queue<int> second (myints.begin(), myints.end());
  
  //queue creation from vector
  std::priority_queue<int> third (arr.begin(), arr.end());

  // greater int is used to make this queue order in the opposite sense i.e the top element now is the smallest.
  std::priority_queue<int, std::vector<int>, std::greater<int> > fourth (myints.begin(), myints.end());
  
  return 0;
}

```

**[Run Code](https://rextester.com/WNCHA7591)
