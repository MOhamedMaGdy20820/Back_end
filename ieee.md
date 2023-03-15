# How The Web Works ? 

Client sends a request A user opens a web browser, such as Google or Chrome  and types in a URL or clicks on a link to request a webpage.

The request is sent from the user's computer to a server

The server receives the request, reads the HTTP headers, and checks the URL to determine which page the user wants.

The server retrieves the requested page and sends it back to the user's computer 

The user's browser receives the response and displays the page in the browser window

User interacts with page The user can interact with the page by clicking on links, filling out forms, or interacting with any dynamic elements of the page.

The process repeats as the user navigates to other pages by clicking on links or typing in new URLs.

<br><br>

# The client-server model

is a computing architecture that describes the relationship between  the client and the server. In this model, the client is a computer or device that requests resources or services from a server
server is another computer or device that provides those resources or services.

 when a user opens a web browser and types in a URL, the browser acts as the client, sending a request to the server hosting the website. The server then responds by sending the requested webpage back to the client, which the browser displays for the user.
<br><br>

# what are class and object in OOP ? and what is the difference between them
a class is a blueprint or template for creating objects. It defines a set of attributes and methods that objects of that class will have

In simpler terms, a class is like a blueprint or a plan for creating objects, while an object is the actual implementation or instance of that plan.

difference between a class and an object is that a class is a template for creating objects, while an object is an instance of a class with its own values for the attributes defined in the class.

`بالبلدى`

Class :<br>
هوه ذي استماره فيها خصائص معينه ممكن تكون ذي الطول الوزن النوع السن ... ألخ

object :<br>
هوه كل شخص هيشتري الأستماره دي و يملاها بخصائصه الخاصه
<br><br>

#  Write a code that takes an array and returns the second largest element of it

```cpp
#include <bits/stdc++.h>
#include <iostream>
#include <string>
#define FIO cin.tie(0), cin.sync_with_stdio(0)
using namespace std;
typedef long long ll;
#define all(x) x.begin(), x.end()
#define fast cin.tie(0); cin.sync_with_stdio(0); cout.tie(0);
void fastIO(void) {
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    cout.tie(NULL);
}

int main()
{
    fastIO();
    int n,k;cin>>n;

    // Solution  one
   /* set <int>a;
    a.emplace(0);
    for (int i = 0; i < n; ++i) {
        cin>>k;
        a.emplace(k);
    }
    cout<<*----a.end();*/
    //----------------------------------------------------------
    // Solution  two

    int arr[n];
    for (int i = 0; i <n ; ++i) {
        cin>>arr[i];
    }

    int mx1=0,mx2=0;

    for (int i = 0; i < n; ++i) {

        if(arr[i]>mx2)
        {
            if(arr[i]>mx1)
            {
                mx2=mx1;
                mx1=arr[i];
            }
            else {
                if(mx1==arr[i])continue;
                mx2 = arr[i];
            }

        }

    }
    cout<<mx2;

    return 0;
}

```

# Write a code that takes a lowercase string and returns the first non-repeating character in it
```cpp
#include <bits/stdc++.h>
#include <iostream>
#include <string>
#define FIO cin.tie(0), cin.sync_with_stdio(0)
using namespace std;
typedef long long ll;
#define all(x) x.begin(), x.end()
#define fast cin.tie(0); cin.sync_with_stdio(0); cout.tie(0);
void fastIO(void) {
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    cout.tie(NULL);
}
int arr[26];

int main()
{
    string s;cin>>s;

    for (int i = 0; i < s.size(); ++i) {
        arr[s[i]-'a']++;
    }

    for (int i = 0; i < s.size(); ++i) {
        if(arr[s[i]-'a']==1)
        {
            cout<<s[i];
            return 0;
        }
    }
    cout<<"all characters repeated ";
    return 0;
}
```