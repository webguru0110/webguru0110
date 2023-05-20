## Student: What is bivariate data?

Mentor: Bivariate data is data that involves two different variables whose values can change. 
Bivariate data deals with relationships between these two variables.
The purpose of bivariate data is to analyze and explain this relationship.

## Student: Is all data bivariate?

Mentor: Actually, some data has only one variable.
For example, if I were to record the ages of all students in a school and graph my data, 
then there would only be one variable, the age of the students.
This type of data is known as univariate data and it does not deal with relationships, but rather it is used to describe something. 
In this example univariate data is used to express the ages of the students in a school.


## What is normal distribution?

Normal distribution, also known as the Gaussian distribution, is a probability distribution that is symmetric about the mean, 
showing that data near the mean are more frequent in occurrence than data far from the mean.

## Can mean and variance can be the same? When will they be different?
for poison distribution mean and variance be same..


MULTITHTREADING ,MULTITASKING AND MULTIPROGRAMMMING
Multiprogramming is the ability for more than one user to use the computer at a time using a single CPU. 
The idea is to effectively utilize the processor to create multiple ready-to-run processes with each process belongs to 
different user.
Multitasking means concurrent execution of multiple processes by one user on the same computer utilizing multiplenCPUs.



## Diffrence between hashtable and hashmap?
Hashtable is synchronized, whereas HashMap is not. This makes HashMap better for non-threaded applications,
as unsynchronized Objects typically perform better than synchronized ones.

Hashtable does not allow null keys or values. HashMap allows one null key and any number of null values.



## What is a Hash Function?

A function that converts a given big phone number to a small practical integer value.
The mapped integer value is used as an index in the hash table.
In simple terms, a hash function maps a big number or string to a small integer that can be used as the index in the hash table.

The mod method:
In this method for creating hash functions,
we map a key into one of the slots of table by taking the remainder of key divided by table_size.
That is, the hash function is
h(key) = key mod table_size 

i.e. key % table_size



The multiplication method:
In multiplication method, we multiply the key k by a constant real number c in the range 0 < c < 1 and 
extract the fractional part of k * c.
Then we multiply this value by table_size m and take the floor of the result. It can be represented as
h(k) = floor (m * (k * c mod 1))
                     or
h(k) = floor (m * frac (k * c))


## How does a text editor work under the hood(in terms of data structures)?

* Rope data structure,
* gap buffer
* peice table..


Given an array, find the longest consecutive sequence. You can find it  https://www.geeksforgeeks.org/longest-consecutive-subsequence/


## OSI MODEL?

OSI (Open Systems Interconnection) is a reference model for how applications communicate over a network.
IT professionals use OSI to model or trace how data is sent or received over a network.
This model breaks down data transmission over a series of seven layers, 
each of which is responsible for performing specific tasks concerning sending and receiving data.
The seven layers of function are provided by a combination of applications, operating systems, network card device drivers 
and networking hardware that 
enable a system to transmit a signal over a network Ethernet or fiber optic cable or through Wi-Fi or other wireless protocols.

1.PHYSICAL LAYER;;  bit synchronization,bit rate control,transmission mode,actual transfer of bits.* Hub, Repeater, Modem, Cables are Physical Layer devices.
                     The major protocols used by this layer include Bluetooth, PON, OTN, DSL, IEEE.802.11, IEEE.802.3, L431 and TIA 449.
2.DATA LINK LAYER:  :node to node delivery of the message., it is the responsibility of DLL to transmit it to the Host using its MAC address.
                     framing,error control,flow control,hysical addressing,access control.* Data Link layer is handled by the NIC (Network Interface Card) 
                     and device drivers of host machines.*** Switch & Bridge are Data Link Layer devices.
                     The protocols are used by the Data Link Layer include: ARP, CSLIP, HDLC, IEEE.802.3, PPP, X-25, SLIP, ATM, SDLS and PLIP.
 3.NETWORK LAYER:: transmission of data from one host to the other located in different networks.Routing and logical addressing
                    Internet Protocol (IPv4), Internet Protocol (IPv6), IPX, AppleTalk, ICMP, IPSec and IGMP.
 4.TRANSPORT LAYER:: data in the transport layer is referred to as Segments. 
                    It is responsible for the End to End delivery of the complete message
                    performed by OS,connectionless or connection oriented,port number.
                     Transmission Control Protocol (TCP), UDP, SPX, DCCP and SCTP.
 5.SESSION LAYER::   Session establishment, maintenance,authentication and termination,SYNCHROMIZATION.
                       The protocols used are: PPTP, SAP, L2TP and NetBIOS.
 6.PRESENTATION LAYER:: Translation,encryption/decryption,compression.The following are the presentation layer protocols: XDR, TLS, SSL and MIME.
 7.APPLICATION LAYER:: Browser,skype,etc..HTTP, SMTP, DHCP, FTP, Telnet, SNMP and SMPP.

 
 OSI model acts as a reference model and is not implemented in Internet because of its late invention. 
 Current model being used is the TCP/IP model.

 
 
## ques : Explain different types of RAID in DBMS?
redundancy array of the independent disk.
It is a technology which is used to connect multiple secondary storage devices for increased performance, data redundancy or both.
It gives you the ability to survive one or more drive failure depending upon the RAID level used.


## RAID
RAID refers to redundancy array of the independent disk. It is a technology which is used to connect multiple secondary storage devices for increased performance, data redundancy or both. It gives you the ability to survive one or more drive failure depending upon the RAID level used.

It consists of an array of disks in which multiple disks are connected to achieve different goals.

RAID technology
There are 7 levels of RAID schemes. These schemas are as RAID 0, RAID 1, ...., RAID 6.


These levels contain the following characteristics:

It contains a set of physical disk drives.
In this technology, the operating system views these separate disks as a single logical disk.
In this technology, data is distributed across the physical drives of the array.
Redundancy disk capacity is used to store parity information.
In case of disk failure, the parity information can be helped to recover the data.
 
 RAID 0 :: data can place inside multple disk,no fault tolerance,once data is lost not recovered.high performance and throughput
 RAID 1 :: copies data from one drive to another,expense is high
 RAID 2 ::  bit-level striping using hamming code parity,
             each data bit in a word is recorded on a separate disk and ECC code of data words is stored on different set disks
             Due to its high cost and complex structure, this level is not commercially used. 
             This same performance can be achieved by RAID 3 at a lower cost.
 RAID 3 ::   RAID 3 consists of byte-level striping with dedicated parity.In case of drive failure, the parity drive is accessed,
             and data is reconstructed from the remaining devices.
             Once the failed drive is replaced, the missing data can be restored on the new drive.
             High speed data transmission.slow performance,data is accessed in parallel.require atleast 3 disk.
RAID 4 ::    block-level stripping with a parity disk. Instead of duplicating data, the RAID 4 adopts a parity-based approach.
             require at least 3 disk,,recover 1 disk only at a time..
RAID 5 ::  block-level striping with DISTRIBUTED parity.same as raid 4.
RAID 6 ::   block-level stripping with 2 parity bits.survive 2 concurrent disk failures,
             This level performs RAID 0 to strip data and RAID 1 to mirror. In this level, stripping is performed before mirroring.
            In this level, drives required should be multiple of 2.
            It is not utilized 100% disk capability as half is used for mirroring.
            It contains very limited scalability.
            
            
## question :: difference between Zero and NULL Character?  

       NULL is used for pointers only as it is defined as (void *) 0. It should not be used other than pointers. 
       If NULL is assigned to a pointer, then pointer is pointing to nothing.
       0 (zero) is a value.
    
##  Explain Different types of Machine Learning with example.
 SUPERVISED :regresion and classification.
 UNSUPERVISED :clustering(group similar data together).
REINFORCEMENT:

REALLIFE EXAMPLE OF OOPS COMCEPTS
ENCAPSULATION:  presence of data and functions manipulating data together.
Encapsulation is a method for protecting data from unwanted access or alteration by packaging it in an object
where it is only accessible through the object's interface. 
Encapsulation are often referred to as information hiding. 
INHERITANCE:
ABSTRACTION:hiding our irrelevanced data;for ex to use a loptop we dont need to know how internal hardwware works.
POLYMORPHISM:Polymorphism is the ability of an object to take on many forms.
The most common use of polymorphism in OOP occurs when a parent class reference is used to refer to a child class object.


encapsulation example:
When you log into your email accounts such as Gmail, Yahoo mail, or Rediff mail, there is a lot of internal processes taking place in the backend and you have no control over it. 
When you enter the password for logging, they are retrieved in an encrypted form and verified and then you are given the access to your account. 
You do not have control over it that how the password has been verified. Thus, it keeps our account safe from being misused.



## operators which cannot be overloaded?
"."  member access op
"?:" ternary condiational op
"sizeOf" 
"typeid"
".*" pointer to member op
"::" scope resoltion op




## CLOUD COMPUTING BASICS
                       AWS, Azure, Google Cloud,IAAS,PAAS,SAAS
                      private cloud,public cloud(B2C) ,hybrid cloud(B2B,B2C),community cloud
                      
                       
## What Are the Different Authentication Factors?
Whether a user is accessing his email or the corporate payroll files, he needs to verify his identity before that access is granted. There are three possible ways this user can prove he is who he claims to be:

Knowledge—the user provides information only he knows, like a password or answers to challenge questions
Possession—the user supplies an item he has, like a YubiKey or a one-time password
Inherence—the user relies on a characteristic unique to who he is, such as a fingerprint, retina scan, or voice recognition
The difference between MFA and 2FA is simple. 
Two-factor authentication always utilizes two of these factors to verify the user’s identity.
Multi-factor authentication could involve two of the factors or it could involve all three.
“Multi-factor” just means any number of factors greater than one.

Continuous Integration (CI) is a development practice that requires developers to integrate code into a shared repository several times a day. 
Each check-in is then verified by an automated build, allowing teams to detect problems early.
By integrating regularly, you can detect errors quickly, and locate them more easily.


## Continuous Integration brings multiple benefits to your organization:

Say goodbye to long and tense integrations
Increase visibility enabling greater communication
Catch issues early and nip them in the bud
Spend less time debugging and more time adding features
Build a solid foundation
Stop waiting to find out if your code’s going to work
Reduce integration problems allowing you to deliver software more rapidly


## LCA of binary tree

```
using namespace std; 
  
// A Binary Tree node 
struct Node 
{ 
    int key; 
    struct Node *left, *right; 
}; 
  
// Utility function creates a new binary tree node with given key 
Node * newNode(int k) 
{ 
    Node *temp = new Node; 
    temp->key = k; 
    temp->left = temp->right = NULL; 
    return temp; 
} 
  
// Finds the path from root node to given root of the tree, Stores the 
// path in a vector path[], returns true if path exists otherwise false 
bool findPath(Node *root, vector<int> &path, int k) 
{ 
    // base case 
    if (root == NULL) return false; 
  
    // Store this node in path vector. The node will be removed if 
    // not in path from root to k 
    path.push_back(root->key); 
  
    // See if the k is same as root's key 
    if (root->key == k) 
        return true; 
  
    // Check if k is found in left or right sub-tree 
    if ( (root->left && findPath(root->left, path, k)) || 
         (root->right && findPath(root->right, path, k)) ) 
        return true; 
  
    // If not present in subtree rooted with root, remove root from 
    // path[] and return false 
    path.pop_back(); 
    return false; 
} 
  
// Returns LCA if node n1, n2 are present in the given binary tree, 
// otherwise return -1 
int findLCA(Node *root, int n1, int n2) 
{ 
    // to store paths to n1 and n2 from the root 
    vector<int> path1, path2; 
  
    // Find paths from root to n1 and root to n1. If either n1 or n2 
    // is not present, return -1 
    if ( !findPath(root, path1, n1) || !findPath(root, path2, n2)) 
          return -1; 
  
    /* Compare the paths to get the first different value */
    int i; 
    for (i = 0; i < path1.size() && i < path2.size() ; i++) 
        if (path1[i] != path2[i]) 
            break; 
    return path1[i-1]; 
} 
  
// Driver program to test above functions 
int main() 
{ 
    // Let us create the Binary Tree shown in above diagram. 
    Node * root = newNode(1); 
    root->left = newNode(2); 
    root->right = newNode(3); 
    root->left->left = newNode(4); 
    root->left->right = newNode(5); 
    root->right->left = newNode(6); 
    root->right->right = newNode(7); 
    cout << "LCA(4, 5) = " << findLCA(root, 4, 5); 
    cout << "nLCA(4, 6) = " << findLCA(root, 4, 6); 
    cout << "nLCA(3, 4) = " << findLCA(root, 3, 4); 
    cout << "nLCA(2, 4) = " << findLCA(root, 2, 4); 
    return 0; 
} 


```


1: Given a list of Students and Subjects along with credits of each, a student can select only those subjects whose credits are less than equal to his/her credits.
Return the number of pairs of students and subjects.
e.g:
Subjects:{3,4,1,2}
students:{5,3}

So there can be 7 pairs as The Student having 5 credits can select all the subjects and the student having credits 3 can select subjects with credits 1,2,3.
Easy Binary search and sort question.




Socket programming in java
// SimpleServer.java: A simple server program.
import java.net.*;
import java.io.*;
public class SimpleServer {
 public static void main(String args[]) throws IOException {
 // Register service on port 1254
 ServerSocket s = new ServerSocket(1254);
 Socket s1=s.accept(); // Wait and accept a connection
 // Get a communication stream associated with the socket
 OutputStream s1out = s1.getOutputStream();
 DataOutputStream dos = new DataOutputStream (s1out);
 // Send a string!
 dos.writeUTF(“Hi there”);
 // Close the connection, but not the server socket
 dos.close();
 s1out.close();
 s1.close();
 }
}


// SimpleClient.java: A simple client program.
import java.net.*;
import java.io.*;
public class SimpleClient {
 public static void main(String args[]) throws IOException {
 // Open your connection to a server, at port 1254
 Socket s1 = new Socket(“localhost”,1254);
 // Get an input file handle from the socket and read the input
 InputStream s1In = s1.getInputStream();
 DataInputStream dis = new DataInputStream(s1In);
 String st = new String (dis.readUTF());
 System.out.println(st);
 // When done, just close the connection and exit
 dis.close();
 s1In.close();
 s1.close();
 }
}




Go – Back – N ARQ

Go – Back – N ARQ provides for sending multiple frames before receiving the acknowledgment for the first frame.
It uses the concept of sliding window, and so is also called sliding window protocol.
The frames are sequentially numbered and a finite number of frames are sent.
If the acknowledgment of a frame is not received within the time period, all frames starting from that frame are retransmitted.

Selective Repeat ARQ

This protocol also provides for sending multiple frames before receiving the acknowledgment for the first frame.
However, here only the erroneous or lost frames are retransmitted, while the good frames are received and buffered.

loss data real life example

AMAG Pharmaceuticals....
Alzheimer’s Association



Implement cloud on your pc.???
To turn your PC into a file server which can transfer files you may use PeerServer.This software makes your PC a private cloud server. 
To access to your file you need this software that makes your PC a client for the server,so it can receive documents, pictures or others.


What happens when we type website name in the browser???
you enter a URL into a web browser
The browser looks up the IP address for the domain name via DNS
The browser sends a HTTP request to the server
The server sends back a HTTP response
The browser begins rendering the HTML
The browser sends requests for additional objects embedded in HTML (images, css, JavaScript) and repeats steps 3-5.
Once the page is loaded, the browser sends further async requests as needed.
            
            
diff bet ipv4 and ipv6
IPv4 has 32-bit address length                        ''''|''''	IPv6 has 128-bit address length
It Supports Manual and DHCP address           ''''|'''' configuration	It supports Auto and renumbering address configuration
In IPv4 end to end connection integrity is Unachievable''''|''''	In IPv6 end to end connection integrity is Achievable
It can generate 4.29×109 address space''''|''''	Address space of IPv6 is quite large it can produce 3.4×1038 address space
Security feature is dependent on application''''|''''	IPSEC is inbuilt security feature in the IPv6 protocol
Address representation of IPv4 in decimal	Address''''|'''' Representation of IPv6 is in hexadecimal
Fragmentation performed by Sender and forwarding routers	''''|''''In IPv6 fragmentation performed only by sender
In IPv4 Packet flow identification is not available''''|''''	In IPv6 packetflow identification are Available and uses flow label field in the header
In IPv4 checksumfield is available''''|''''	In IPv6 checksumfield is not available
It has broadcast Message Transmission Scheme''''|''''	In IPv6 multicast and any cast message transmission scheme is available
In IPv4 Encryption and Authentication facility not provided''''|'''''	In IPv6 Encryption and Authentication are provided
            
    
    
   3G
   
    10mbps
    packet switching
    wide area network architecture
    uses turbo codes for error correction
    CDMA technology,UMTS
    
    4G
    100mbps
    packet and message switching
    integration of wide area and wireless lan architecture
    uses concatenated codes for error correction
    OFDMA,LTE
    
    
    
    Working of DNS and its server???
    The Domain Name Systems (DNS) is the phonebook of the Internet. 
    Humans access information online through domain names, like nytimes.com or espn.com.
    Web browsers interact through Internet Protocol (IP) addresses. 
    DNS translates domain names to IP addresses so browsers can load Internet resources.

Each device connected to the Internet has a unique IP address which other machines use to find the device.
DNS servers eliminate the need for humans to memorize IP addresses such as 192.168.1.1 (in IPv4), 
or more complex newer alphanumeric IP addresses such as 2400:cb00:2048:1::c629:d7a2 (in IPv6).


LAN Network ----ethernet  and token ring technolgies
WAN Network ----frame relay,ATM,X.25

C support only procedural programming while C++ support both procedural and OOPs.
c was by Denis Ritchie 1969 at bell labsand C++ bjarne stroustrup in 1979.
no operator and function overloading in C,no virtual and friend function,
No direct support for Error Handling in C.....


volatile specifies a variable whose value may be changed by processes outside the current program

Singleton Class in Java
In object-oriented programming, a singleton class is a class that can have only one object (an instance of the class) at a time.
To design a singleton class:

Make constructor as private.
Write a static method that has return type object of this singleton class. 
Here, the concept of Lazy initialization in used to write this static method.


Storage cLasses in C
auto
register
extern
static


Register(store on cpu register).
if a variable is declared register, the unary & (address of) operator may not be applied to it, 
Variables belonging to register storage class are local to the block which they are defined in,
and get destroyed on exit from the block.


ALL varaibles in C normallly impliitily defined  as auto...store at stack....
EXTERN -global variable.
.The main purpose of using extern variables is that they can be accessed between two different files 
which are part of a large program.


Dynamic memory allocation in C
malloc()----single large block of memory for eg int* ptr=(int*) malloc(20bytes);|  20 bytes    |  
calloc ----contigious allocation of memory for eg int* arr=(int*) calloc(5*sizeOf(int));   | | | | | | 5 blocks of 4 bytes
realloc---to increase the previous alloted memory for above we define ptr and now we want to increase its memory 
ptr=realloc(ptr,newSize);


Operating sysytem,C++,java,computer Networks................................................................


Find the number of sub-strings in a given string where each sub-string has the same character in beginning and end
Method 3 (Best approach) : Now if we carefully observe then we can realize that the answer just depends on frequencies of characters in the original string. For example in string abcab, frequency of ‘a’ is 2 and substrings contributing to answer are a, abca and a respectively, a total of 3, which is calculated by (frequency of ‘a’+1)C2.
filter_none
edit
play_arrow

brightness_4
// Most efficient C++ program to count all   
// substrings with same first and last characters. 
#include <bits/stdc++.h> 
using namespace std; 
const int MAX_CHAR = 26;  // assuming lower case only 
  
int countSubstringWithEqualEnds(string s) 
{ 
    int result = 0; 
    int n = s.length(); 
  
    // Calculating frequency of each character 
    // in the string. 
    int count[MAX_CHAR] = {0}; 
    for (int i=0; i<n; i++) 
        count[s[i]-'a']++; 
  
    // Computing result using counts 
    for (int i=0; i<MAX_CHAR; i++) 
        result += (count[i]*(count[i]+1)/2); 
  
    return result; 
} 
  
// Driver function 
int main() 
{ 
    string s("abcab"); 
    cout << countSubstringWithEqualEnds(s); 
    return 0; 
} 





Finf sum of  longest path from root to leaf node?.
using namespace std; 
  
// Node of a binary tree 
struct Node { 
    int data; 
    Node* left, *right; 
}; 
  
// function to get a new node 
Node* getNode(int data) 
{ 
    // allocate memory for the node 
    Node* newNode = (Node*)malloc(sizeof(Node)); 
  
    // put in the data 
    newNode->data = data; 
    newNode->left = newNode->right = NULL; 
    return newNode; 
} 
  
// function to find the sum of nodes on the 
// longest path from root to leaf node 
void sumOfLongRootToLeafPath(Node* root, int sum, 
                      int len, int& maxLen, int& maxSum) 
{ 
    // if true, then we have traversed a 
    // root to leaf path 
    if (!root) { 
        // update maximum length and maximum sum 
        // according to the given conditions 
        if (maxLen < len) { 
            maxLen = len; 
            maxSum = sum; 
        } else if (maxLen == len && maxSum < sum) 
            maxSum = sum; 
        return; 
    } 
  
    // recur for left subtree 
    sumOfLongRootToLeafPath(root->left, sum + root->data, 
                            len + 1, maxLen, maxSum); 
  
    // recur for right subtree 
    sumOfLongRootToLeafPath(root->right, sum + root->data, 
                            len + 1, maxLen, maxSum); 
} 
  
// utility function to find the sum of nodes on 
// the longest path from root to leaf node 
int sumOfLongRootToLeafPathUtil(Node* root) 
{ 
    // if tree is NULL, then sum is 0 
    if (!root) 
        return 0; 
  
    int maxSum = INT_MIN, maxLen = 0; 
  
    // finding the maximum sum 'maxSum' for the 
    // maximum length root to leaf path 
    sumOfLongRootToLeafPath(root, 0, 0, maxLen, maxSum); 
  
    // required maximum sum 
    return maxSum; 
} 
  
// Driver program to test above 
int main() 
{ 
    // binary tree formation 
    Node* root = getNode(4);         /*        4        */
    root->left = getNode(2);         /*       / \       */
    root->right = getNode(5);        /*      2   5      */
    root->left->left = getNode(7);   /*     / \ / \     */
    root->left->right = getNode(1);  /*    7  1 2  3    */
    root->right->left = getNode(2);  /*      /          */
    root->right->right = getNode(3); /*     6           */
    root->left->right->left = getNode(6); 
  
    cout << "Sum = "
         << sumOfLongRootToLeafPathUtil(root); 
  
    return 0; 
} 

 
 
 Reverse individual words with O(1) extra space??
 string reverseWords(string str) 
{ 
  
    // Pointer to the first character 
    // of the first word 
    int start = 0; 
    for (int i = 0; i <= str.size(); i++) { 
  
        // If the current word has ended 
        if (str[i] == ' ' || i == str.size()) { 
  
            // Pointer to the last character 
            // of the current word 
            int end = i - 1; 
  
            // Reverse the current word 
            while (start < end) { 
                swap(str[start], str[end]); 
                start++; 
                end--; 
            } 
  
            // Pointer to the first character 
            // of the next word 
            start = i + 1; 
        } 
    } 
  
    return str; 
} 



. Fractional knapsack and implementing it using dynamic programming ( modify 01 knapsack).??
using namespace std; 
  
// Structure for an item which stores weight and corresponding 
// value of Item 
struct Item 
{ 
    int value, weight; 
  
    // Constructor 
    Item(int value, int weight) : value(value), weight(weight) 
    {} 
}; 
  
// Comparison function to sort Item according to val/weight ratio 
bool cmp(struct Item a, struct Item b) 
{ 
    double r1 = (double)a.value / a.weight; 
    double r2 = (double)b.value / b.weight; 
    return r1 > r2; 
} 
  
// Main greedy function to solve problem 
double fractionalKnapsack(int W, struct Item arr[], int n) 
{ 
    //    sorting Item on basis of ratio 
    sort(arr, arr + n, cmp); 
  
    //    Uncomment to see new order of Items with their ratio 
    /* 
    for (int i = 0; i < n; i++) 
    { 
        cout << arr[i].value << "  " << arr[i].weight << " : " 
             << ((double)arr[i].value / arr[i].weight) << endl; 
    } 
    */
  
    int curWeight = 0;  // Current weight in knapsack 
    double finalvalue = 0.0; // Result (value in Knapsack) 
  
    // Looping through all Items 
    for (int i = 0; i < n; i++) 
    { 
        // If adding Item won't overflow, add it completely 
        if (curWeight + arr[i].weight <= W) 
        { 
            curWeight += arr[i].weight; 
            finalvalue += arr[i].value; 
        } 
  
        // If we can't add current Item, add fractional part of it 
        else
        { 
            int remain = W - curWeight; 
            finalvalue += arr[i].value * ((double) remain / arr[i].weight); 
            break; 
        } 
    } 
  
    // Returning final value 
    return finalvalue; 
}




Longest palindromic substring

 int longestPalSubstr(string str) 
{ 
    // get length of input string 
    int n = str.size();  
  
    // table[i][j] will be false if substring str[i..j] 
    // is not palindrome. 
    // Else table[i][j] will be true 
    bool table[n][n]; 
      
    memset(table, 0, sizeof(table)); 
  
    // All substrings of length 1 are palindromes 
    int maxLength = 1; 
      
    for (int i = 0; i < n; ++i) 
        table[i][i] = true; 
  
    // check for sub-string of length 2. 
    int start = 0; 
    for (int i = 0; i < n-1; ++i) 
    { 
        if (str[i] == str[i+1]) 
        { 
            table[i][i+1] = true; 
            start = i; 
            maxLength = 2; 
        } 
    } 
  
    // Check for lengths greater than 2. k is length 
    // of substring 
    for (int k = 3; k <= n; ++k) 
    { 
        // Fix the starting index 
        for (int i = 0; i < n-k+1 ; ++i) 
        { 
            // Get the ending index of substring from 
            // starting index i and length k 
            int j = i + k - 1; 
  
            // checking for sub-string from ith index to 
            // jth index iff str[i+1] to str[j-1] is a 
            // palindrome 
            if (table[i+1][j-1] && str[i] == str[j]) 
            { 
                table[i][j] = true; 
  
                if (k > maxLength) 
                { 
                    start = i; 
                    maxLength = k; 
                } 
            } 
        } 
    } 
  
   cout << "Longest palindrome substring is: "; 
   printSubStr( str, start, start + maxLength - 1 ); 
      
    // return length of LPS 
    return maxLength; 
} 

Application of DFS and BFS.
1) Shortest Path and Minimum Spanning Tree for unweighted graph In an unweighted graph, the shortest path is the path with least 
number of edges. With Breadth First, we always reach a vertex from given source using the minimum number of edges.
Also, in case of unweighted graphs, any spanning tree is Minimum Spanning Tree and we can use either Depth or Breadth first 
traversal for finding a spanning tree.

2) Peer to Peer Networks. In Peer to Peer Networks like BitTorrent, Breadth First Search is used to find all neighbor nodes.

3) Crawlers in Search Engines: Crawlers build index using Breadth First. The idea is to start from source page and follow all
links from source and keep doing same. Depth First Traversal can also be used for crawlers, but the advantage with Breadth First
Traversal is, depth or levels of the built tree can be limited.

4) Social Networking Websites: In social networks, we can find people within a given distance ‘k’ from a person using Breadth
First Search till ‘k’ levels.

5) GPS Navigation systems: Breadth First Search is used to find all neighboring locations.

6) Broadcasting in Network: In networks, a broadcasted packet follows Breadth First Search to reach all nodes.

7) In Garbage Collection: Breadth First Search is used in copying garbage collection using Cheney’s algorithm. Refer this and for
details. Breadth First Search is preferred over Depth First Search because of better locality of reference:

8) Cycle detection in undirected graph: In undirected graphs, either Breadth First Search or Depth First Search can be used to
detect cycle. In directed graph, only depth first search can be used.

9) Ford–Fulkerson algorithm In Ford-Fulkerson algorithm, we can either use Breadth First or Depth First Traversal to find the
maximum flow. Breadth First Traversal is preferred as it reduces worst case time complexity to O(VE2).

10) To test if a graph is Bipartite We can either use Breadth First or Depth First Traversal.

11) Path Finding We can either use Breadth First or Depth First Traversal to find if there is a path between two vertices.

12) Finding all nodes within one connected component: We can either use Breadth First or Depth First Traversal to find all nodes
reachable from a given node.

Many algorithms like Prim’s Minimum Spanning Tree and Dijkstra’s Single Source Shortest Path use structure similar to Breadth
First Search.


os questions 
What is the difference between Mutex and Binary Semaphore though they work same?
mutex is a locking mechanaism and semphaphore is a signalling mechansim

What is difference between MAC address and IP address?
48 bits mac and 32 bits IP
mac is on NIC card,.IP is assigned by ISP
ARP retrieve MAc and RARP retrieve IP.




Difference between hub, switch and routers?
hub braodcast message Layer 1 of OSI
switch send data to specific location layer 2 off OSI
Router is used to connect two networks layer 3 of OSI






what isDHCP?
A DHCP server enables computers to request IP addresses 
and networking parameters automatically from the Internet service provider 





What is piggybacking?
In two-way communication, wherever a frame is received, the receiver waits and does not send the control frame (acknowledgement or ACK) back to the sender immediately.

The receiver waits until its network layer passes in the next data packet. The delayed acknowledgement is then attached to this outgoing data frame.

This technique of temporarily delaying the acknowledgement so that it can be hooked with next outgoing data frame is known as piggybacking.


What is flooding in routers?
Flooding is used in computer networks routing algorithm in which every incoming packet is sent through every outgoing link except the one it arrived on




Explain 3 way handshake connection establishment process in TCP?
TCP 3-way handshake

To establish a connection, TCP uses a three-way handshake. Before a client attempts to connect with a server, the server must 
first bind to and listen at a port to open it up for connections: this is called a passive open. Once the passive open is 
established, a client may initiate an active open. To establish a connection, the three-way (or 3-step) handshake occurs:

SYN(sequence number): The active open is performed by the client sending a SYN to the server. The client sets the segment's sequence number to
a random value A.
SYN-ACK: In response, the server replies with a SYN-ACK. The acknowledgment number is set to one more than the received
sequence number i.e. A+1, and the sequence number that the server chooses for the packet is another random number, B.
ACK: Finally, the client sends an ACK back to the server. The sequence number is set to the received acknowledgement value 
i.e. A+1, and the acknowledgement number is set to one more than the received sequence number i.e. B+1.
At this point, both the client and server have received an acknowledgment of the connection. The steps 1, 2 establish the 
onnection parameter (sequence number) for one direction and it is acknowledged. The steps 2, 3 establish the connection 
parameter (sequence number) for the other direction and it is acknowledged. With these, a full-duplex communication is 
established.

Number of subarrays having sum exactly equal to k?
// with sum exactly equal to k. 
#include <bits/stdc++.h> 
using namespace std; 
  
// Function to find number of subarrays  
// with sum exactly equal to k. 
int findSubarraySum(int arr[], int n, int sum) 
{ 
    // STL map to store number of subarrays 
    // starting from index zero having  
    // particular value of sum. 
    unordered_map<int, int> prevSum; 
  
    int res = 0; 
  
    // Sum of elements so far. 
    int currsum = 0; 
  
    for (int i = 0; i < n; i++) { 
  
        // Add current element to sum so far. 
        currsum += arr[i]; 
  
        // If currsum is equal to desired sum, 
        // then a new subarray is found. So 
        // increase count of subarrays. 
        if (currsum == sum)  
            res++;         
  
        // currsum exceeds given sum by currsum  
        //  - sum. Find number of subarrays having  
        // this sum and exclude those subarrays 
        // from currsum by increasing count by  
        // same amount. 
        if (prevSum.find(currsum - sum) !=  
                                  prevSum.end())  
            res += (prevSum[currsum - sum]); 
          
  
        // Add currsum value to count of  
        // different values of sum. 
        prevSum[currsum]++; 
    } 
  
    return res; 
} 
  
int main() 
{ 
    int arr[] = { 10, 2, -2, -20, 10 }; 
    int sum = -10; 
    int n = sizeof(arr) / sizeof(arr[0]); 
    cout << findSubarraySum(arr, n, sum); 
    return 0; 
} 


string matching ALGO KMP ???
#include <bits/stdc++.h> 
  
void computeLPSArray(char* pat, int M, int* lps); 
  
// Prints occurrences of txt[] in pat[] 
void KMPSearch(char* pat, char* txt) 
{ 
    int M = strlen(pat); 
    int N = strlen(txt); 
  
    // create lps[] that will hold the longest prefix suffix 
    // values for pattern 
    int lps[M]; 
  
    // Preprocess the pattern (calculate lps[] array) 
    computeLPSArray(pat, M, lps); 
  
    int i = 0; // index for txt[] 
    int j = 0; // index for pat[] 
    while (i < N) { 
        if (pat[j] == txt[i]) { 
            j++; 
            i++; 
        } 
  
        if (j == M) { 
            printf("Found pattern at index %d ", i - j); 
            j = lps[j - 1]; 
        } 
  
        // mismatch after j matches 
        else if (i < N && pat[j] != txt[i]) { 
            // Do not match lps[0..lps[j-1]] characters, 
            // they will match anyway 
            if (j != 0) 
                j = lps[j - 1]; 
            else
                i = i + 1; 
        } 
    } 
} 
  
// Fills lps[] for given patttern pat[0..M-1] 
void computeLPSArray(char* pat, int M, int* lps) 
{ 
    // length of the previous longest prefix suffix 
    int len = 0; 
  
    lps[0] = 0; // lps[0] is always 0 
  
    // the loop calculates lps[i] for i = 1 to M-1 
    int i = 1; 
    while (i < M) { 
        if (pat[i] == pat[len]) { 
            len++; 
            lps[i] = len; 
            i++; 
        } 
        else // (pat[i] != pat[len]) 
        { 
            // This is tricky. Consider the example. 
            // AAACAAAA and i = 7. The idea is similar 
            // to search step. 
            if (len != 0) { 
                len = lps[len - 1]; 
  
                // Also, note that we do not increment 
                // i here 
            } 
            else // if (len == 0) 
            { 
                lps[i] = 0; 
                i++; 
            } 
        } 
    } 
} 
  
// Driver program to test above function 
int main() 
{ 
    char txt[] = "ABABDABACDABABCABAB"; 
    char pat[] = "ABABCABAB"; 
    KMPSearch(pat, txt); 
    return 0; 
}





Student: What is bivariate data?

Mentor: Bivariate data is data that involves two different variables whose values can change. 
Bivariate data deals with relationships between these two variables.
The purpose of bivariate data is to analyze and explain this relationship.

Student: Is all data bivariate?

Mentor: Actually, some data has only one variable.
For example, if I were to record the ages of all students in a school and graph my data, 
then there would only be one variable, the age of the students.
This type of data is known as univariate data and it does not deal with relationships, but rather it is used to describe something. 
In this example univariate data is used to express the ages of the students in a school.


What is normal distribution?

Normal distribution, also known as the Gaussian distribution, is a probability distribution that is symmetric about the mean, 
showing that data near the mean are more frequent in occurrence than data far from the mean.

Can mean and variance can be the same? When will they be different?
for poison distribution mean and variance be same..


MULTITHTREADING ,MULTITASKING AND MULTIPROGRAMMMING
Multiprogramming is the ability for more than one user to use the computer at a time using a single CPU. 
The idea is to effectively utilize the processor to create multiple ready-to-run processes with each process belongs to 
different user.
Multitasking means concurrent execution of multiple processes by one user on the same computer utilizing multiplenCPUs.



Diffrence between hashtable and hashmap?
Hashtable is synchronized, whereas HashMap is not. This makes HashMap better for non-threaded applications,
as unsynchronized Objects typically perform better than synchronized ones.

Hashtable does not allow null keys or values. HashMap allows one null key and any number of null values.



What is a Hash Function?

A function that converts a given big phone number to a small practical integer value.
The mapped integer value is used as an index in the hash table.
In simple terms, a hash function maps a big number or string to a small integer that can be used as the index in the hash table.

The mod method:
In this method for creating hash functions,
we map a key into one of the slots of table by taking the remainder of key divided by table_size.
That is, the hash function is
h(key) = key mod table_size 

i.e. key % table_size



The multiplication method:
In multiplication method, we multiply the key k by a constant real number c in the range 0 < c < 1 and 
extract the fractional part of k * c.
Then we multiply this value by table_size m and take the floor of the result. It can be represented as
h(k) = floor (m * (k * c mod 1))
                     or
h(k) = floor (m * frac (k * c))


How does a text editor work under the hood(in terms of data structures)?
Rope data structure,
gap buffer
peice table..


Given an array, find the longest consecutive sequence. You can find it  https://www.geeksforgeeks.org/longest-consecutive-subsequence/


OSI MODEL?
OSI (Open Systems Interconnection) is a reference model for how applications communicate over a network.
IT professionals use OSI to model or trace how data is sent or received over a network.
This model breaks down data transmission over a series of seven layers, 
each of which is responsible for performing specific tasks concerning sending and receiving data.
The seven layers of function are provided by a combination of applications, operating systems, network card device drivers 
and networking hardware that 
enable a system to transmit a signal over a network Ethernet or fiber optic cable or through Wi-Fi or other wireless protocols.

1.PHYSICAL LAYER;;  bit synchronization,bit rate control,transmission mode,actual transfer of bits.* Hub, Repeater, Modem, Cables are Physical Layer devices.
                     The major protocols used by this layer include Bluetooth, PON, OTN, DSL, IEEE.802.11, IEEE.802.3, L431 and TIA 449.
2.DATA LINK LAYER:  :node to node delivery of the message., it is the responsibility of DLL to transmit it to the Host using its MAC address.
                     framing,error control,flow control,hysical addressing,access control.* Data Link layer is handled by the NIC (Network Interface Card) 
                     and device drivers of host machines.*** Switch & Bridge are Data Link Layer devices.
                     The protocols are used by the Data Link Layer include: ARP, CSLIP, HDLC, IEEE.802.3, PPP, X-25, SLIP, ATM, SDLS and PLIP.
 3.NETWORK LAYER:: transmission of data from one host to the other located in different networks.Routing and logical addressing
                    Internet Protocol (IPv4), Internet Protocol (IPv6), IPX, AppleTalk, ICMP, IPSec and IGMP.
 4.TRANSPORT LAYER:: data in the transport layer is referred to as Segments. 
                    It is responsible for the End to End delivery of the complete message
                    performed by OS,connectionless or connection oriented,port number.
                     Transmission Control Protocol (TCP), UDP, SPX, DCCP and SCTP.
 5.SESSION LAYER::   Session establishment, maintenance,authentication and termination,SYNCHROMIZATION.
                       The protocols used are: PPTP, SAP, L2TP and NetBIOS.
 6.PRESENTATION LAYER:: Translation,encryption/decryption,compression.The following are the presentation layer protocols: XDR, TLS, SSL and MIME.
 7.APPLICATION LAYER:: Browser,skype,etc..HTTP, SMTP, DHCP, FTP, Telnet, SNMP and SMPP.

 
 OSI model acts as a reference model and is not implemented in Internet because of its late invention. 
 Current model being used is the TCP/IP model.
 
 

 
 
 
 
 
 
 
 
 
ques : Explain different types of RAID in DBMS?
redundancy array of the independent disk.
It is a technology which is used to connect multiple secondary storage devices for increased performance, data redundancy or both.
It gives you the ability to survive one or more drive failure depending upon the RAID level used.


next →← prev
RAID
RAID refers to redundancy array of the independent disk. It is a technology which is used to connect multiple secondary storage devices for increased performance, data redundancy or both. It gives you the ability to survive one or more drive failure depending upon the RAID level used.

It consists of an array of disks in which multiple disks are connected to achieve different goals.

RAID technology
There are 7 levels of RAID schemes. These schemas are as RAID 0, RAID 1, ...., RAID 6.


These levels contain the following characteristics:

It contains a set of physical disk drives.
In this technology, the operating system views these separate disks as a single logical disk.
In this technology, data is distributed across the physical drives of the array.
Redundancy disk capacity is used to store parity information.
In case of disk failure, the parity information can be helped to recover the data.
 
 RAID 0 :: data can place inside multple disk,no fault tolerance,once data is lost not recovered.high performance and throughput
 RAID 1 :: copies data from one drive to another,expense is high
 RAID 2 ::  bit-level striping using hamming code parity,
             each data bit in a word is recorded on a separate disk and ECC code of data words is stored on different set disks
             Due to its high cost and complex structure, this level is not commercially used. 
             This same performance can be achieved by RAID 3 at a lower cost.
 RAID 3 ::   RAID 3 consists of byte-level striping with dedicated parity.In case of drive failure, the parity drive is accessed,
             and data is reconstructed from the remaining devices.
             Once the failed drive is replaced, the missing data can be restored on the new drive.
             High speed data transmission.slow performance,data is accessed in parallel.require atleast 3 disk.
RAID 4 ::    block-level stripping with a parity disk. Instead of duplicating data, the RAID 4 adopts a parity-based approach.
             require at least 3 disk,,recover 1 disk only at a time..
RAID 5 ::  block-level striping with DISTRIBUTED parity.same as raid 4.
RAID 6 ::   block-level stripping with 2 parity bits.survive 2 concurrent disk failures,
             This level performs RAID 0 to strip data and RAID 1 to mirror. In this level, stripping is performed before mirroring.
            In this level, drives required should be multiple of 2.
            It is not utilized 100% disk capability as half is used for mirroring.
            It contains very limited scalability.
            
            
question :: difference between Zero and NULL Character?  
       NULL is used for pointers only as it is defined as (void *) 0. It should not be used other than pointers. 
       If NULL is assigned to a pointer, then pointer is pointing to nothing.
       0 (zero) is a value.
    
 Explain Different types of Machine Learning with example.
 SUPERVISED :regresion and classification.
 UNSUPERVISED :clustering(group similar data together).
REINFORCEMENT:

REALLIFE EXAMPLE OF OOPS COMCEPTS
ENCAPSULATION:  presence of data and functions manipulating data together.
Encapsulation is a method for protecting data from unwanted access or alteration by packaging it in an object
where it is only accessible through the object's interface. 
Encapsulation are often referred to as information hiding. 
INHERITANCE:
ABSTRACTION:hiding our irrelevanced data;for ex to use a loptop we dont need to know how internal hardwware works.
POLYMORPHISM:Polymorphism is the ability of an object to take on many forms.
The most common use of polymorphism in OOP occurs when a parent class reference is used to refer to a child class object.


encapsulation example:
When you log into your email accounts such as Gmail, Yahoo mail, or Rediff mail, there is a lot of internal processes taking place in the backend and you have no control over it. 
When you enter the password for logging, they are retrieved in an encrypted form and verified and then you are given the access to your account. 
You do not have control over it that how the password has been verified. Thus, it keeps our account safe from being misused.



operators which cannot be overloaded?
"."  member access op
"?:" ternary condiational op
"sizeOf" 
"typeid"
".*" pointer to member op
"::" scope resoltion op




CLOUD COMPUTING BASICS
                       AWS, Azure, Google Cloud,IAAS,PAAS,SAAS
                      private cloud,public cloud(B2C) ,hybrid cloud(B2B,B2C),community cloud
                      
                       
What Are the Different Authentication Factors?
Whether a user is accessing his email or the corporate payroll files, he needs to verify his identity before that access is granted. There are three possible ways this user can prove he is who he claims to be:

Knowledge—the user provides information only he knows, like a password or answers to challenge questions
Possession—the user supplies an item he has, like a YubiKey or a one-time password
Inherence—the user relies on a characteristic unique to who he is, such as a fingerprint, retina scan, or voice recognition
The difference between MFA and 2FA is simple. 
Two-factor authentication always utilizes two of these factors to verify the user’s identity.
Multi-factor authentication could involve two of the factors or it could involve all three.
“Multi-factor” just means any number of factors greater than one.

Continuous Integration (CI) is a development practice that requires developers to integrate code into a shared repository several times a day. 
Each check-in is then verified by an automated build, allowing teams to detect problems early.
By integrating regularly, you can detect errors quickly, and locate them more easily.


Continuous Integration brings multiple benefits to your organization:

Say goodbye to long and tense integrations
Increase visibility enabling greater communication
Catch issues early and nip them in the bud
Spend less time debugging and more time adding features
Build a solid foundation
Stop waiting to find out if your code’s going to work
Reduce integration problems allowing you to deliver software more rapidly


LCA of binary tree

using namespace std; 
  
// A Binary Tree node 
struct Node 
{ 
    int key; 
    struct Node *left, *right; 
}; 
  
// Utility function creates a new binary tree node with given key 
Node * newNode(int k) 
{ 
    Node *temp = new Node; 
    temp->key = k; 
    temp->left = temp->right = NULL; 
    return temp; 
} 
  
// Finds the path from root node to given root of the tree, Stores the 
// path in a vector path[], returns true if path exists otherwise false 
bool findPath(Node *root, vector<int> &path, int k) 
{ 
    // base case 
    if (root == NULL) return false; 
  
    // Store this node in path vector. The node will be removed if 
    // not in path from root to k 
    path.push_back(root->key); 
  
    // See if the k is same as root's key 
    if (root->key == k) 
        return true; 
  
    // Check if k is found in left or right sub-tree 
    if ( (root->left && findPath(root->left, path, k)) || 
         (root->right && findPath(root->right, path, k)) ) 
        return true; 
  
    // If not present in subtree rooted with root, remove root from 
    // path[] and return false 
    path.pop_back(); 
    return false; 
} 
  
// Returns LCA if node n1, n2 are present in the given binary tree, 
// otherwise return -1 
int findLCA(Node *root, int n1, int n2) 
{ 
    // to store paths to n1 and n2 from the root 
    vector<int> path1, path2; 
  
    // Find paths from root to n1 and root to n1. If either n1 or n2 
    // is not present, return -1 
    if ( !findPath(root, path1, n1) || !findPath(root, path2, n2)) 
          return -1; 
  
    /* Compare the paths to get the first different value */
    int i; 
    for (i = 0; i < path1.size() && i < path2.size() ; i++) 
        if (path1[i] != path2[i]) 
            break; 
    return path1[i-1]; 
} 
  
// Driver program to test above functions 
int main() 
{ 
    // Let us create the Binary Tree shown in above diagram. 
    Node * root = newNode(1); 
    root->left = newNode(2); 
    root->right = newNode(3); 
    root->left->left = newNode(4); 
    root->left->right = newNode(5); 
    root->right->left = newNode(6); 
    root->right->right = newNode(7); 
    cout << "LCA(4, 5) = " << findLCA(root, 4, 5); 
    cout << "nLCA(4, 6) = " << findLCA(root, 4, 6); 
    cout << "nLCA(3, 4) = " << findLCA(root, 3, 4); 
    cout << "nLCA(2, 4) = " << findLCA(root, 2, 4); 
    return 0; 
} 




1: Given a list of Students and Subjects along with credits of each, a student can select only those subjects whose credits are less than equal to his/her credits.
Return the number of pairs of students and subjects.
e.g:
Subjects:{3,4,1,2}
students:{5,3}

So there can be 7 pairs as The Student having 5 credits can select all the subjects and the student having credits 3 can select subjects with credits 1,2,3.
Easy Binary search and sort question.




Socket programming in java
// SimpleServer.java: A simple server program.
import java.net.*;
import java.io.*;
public class SimpleServer {
 public static void main(String args[]) throws IOException {
 // Register service on port 1254
 ServerSocket s = new ServerSocket(1254);
 Socket s1=s.accept(); // Wait and accept a connection
 // Get a communication stream associated with the socket
 OutputStream s1out = s1.getOutputStream();
 DataOutputStream dos = new DataOutputStream (s1out);
 // Send a string!
 dos.writeUTF(“Hi there”);
 // Close the connection, but not the server socket
 dos.close();
 s1out.close();
 s1.close();
 }
}


// SimpleClient.java: A simple client program.
import java.net.*;
import java.io.*;
public class SimpleClient {
 public static void main(String args[]) throws IOException {
 // Open your connection to a server, at port 1254
 Socket s1 = new Socket(“localhost”,1254);
 // Get an input file handle from the socket and read the input
 InputStream s1In = s1.getInputStream();
 DataInputStream dis = new DataInputStream(s1In);
 String st = new String (dis.readUTF());
 System.out.println(st);
 // When done, just close the connection and exit
 dis.close();
 s1In.close();
 s1.close();
 }
}




Go – Back – N ARQ

Go – Back – N ARQ provides for sending multiple frames before receiving the acknowledgment for the first frame.
It uses the concept of sliding window, and so is also called sliding window protocol.
The frames are sequentially numbered and a finite number of frames are sent.
If the acknowledgment of a frame is not received within the time period, all frames starting from that frame are retransmitted.

Selective Repeat ARQ

This protocol also provides for sending multiple frames before receiving the acknowledgment for the first frame.
However, here only the erroneous or lost frames are retransmitted, while the good frames are received and buffered.

loss data real life example

AMAG Pharmaceuticals....
Alzheimer’s Association



Implement cloud on your pc.???
To turn your PC into a file server which can transfer files you may use PeerServer.This software makes your PC a private cloud server. 
To access to your file you need this software that makes your PC a client for the server,so it can receive documents, pictures or others.


What happens when we type website name in the browser???
you enter a URL into a web browser
The browser looks up the IP address for the domain name via DNS
The browser sends a HTTP request to the server
The server sends back a HTTP response
The browser begins rendering the HTML
The browser sends requests for additional objects embedded in HTML (images, css, JavaScript) and repeats steps 3-5.
Once the page is loaded, the browser sends further async requests as needed.
            
            
diff bet ipv4 and ipv6
IPv4 has 32-bit address length                        ''''|''''	IPv6 has 128-bit address length
It Supports Manual and DHCP address           ''''|'''' configuration	It supports Auto and renumbering address configuration
In IPv4 end to end connection integrity is Unachievable''''|''''	In IPv6 end to end connection integrity is Achievable
It can generate 4.29×109 address space''''|''''	Address space of IPv6 is quite large it can produce 3.4×1038 address space
Security feature is dependent on application''''|''''	IPSEC is inbuilt security feature in the IPv6 protocol
Address representation of IPv4 in decimal	Address''''|'''' Representation of IPv6 is in hexadecimal
Fragmentation performed by Sender and forwarding routers	''''|''''In IPv6 fragmentation performed only by sender
In IPv4 Packet flow identification is not available''''|''''	In IPv6 packetflow identification are Available and uses flow label field in the header
In IPv4 checksumfield is available''''|''''	In IPv6 checksumfield is not available
It has broadcast Message Transmission Scheme''''|''''	In IPv6 multicast and any cast message transmission scheme is available
In IPv4 Encryption and Authentication facility not provided''''|'''''	In IPv6 Encryption and Authentication are provided
            
    
    
   3G
   
    10mbps
    packet switching
    wide area network architecture
    uses turbo codes for error correction
    CDMA technology,UMTS
    
    4G
    100mbps
    packet and message switching
    integration of wide area and wireless lan architecture
    uses concatenated codes for error correction
    OFDMA,LTE
    
    
    
    Working of DNS and its server???
    The Domain Name Systems (DNS) is the phonebook of the Internet. 
    Humans access information online through domain names, like nytimes.com or espn.com.
    Web browsers interact through Internet Protocol (IP) addresses. 
    DNS translates domain names to IP addresses so browsers can load Internet resources.

Each device connected to the Internet has a unique IP address which other machines use to find the device.
DNS servers eliminate the need for humans to memorize IP addresses such as 192.168.1.1 (in IPv4), 
or more complex newer alphanumeric IP addresses such as 2400:cb00:2048:1::c629:d7a2 (in IPv6).


LAN Network ----ethernet  and token ring technolgies
WAN Network ----frame relay,ATM,X.25

C support only procedural programming while C++ support both procedural and OOPs.
c was by Denis Ritchie 1969 at bell labsand C++ bjarne stroustrup in 1979.
no operator and function overloading in C,no virtual and friend function,
No direct support for Error Handling in C.....


volatile specifies a variable whose value may be changed by processes outside the current program

Singleton Class in Java
In object-oriented programming, a singleton class is a class that can have only one object (an instance of the class) at a time.
To design a singleton class:

Make constructor as private.
Write a static method that has return type object of this singleton class. 
Here, the concept of Lazy initialization in used to write this static method.


Storage cLasses in C
auto
register
extern
static


Register(store on cpu register).
if a variable is declared register, the unary & (address of) operator may not be applied to it, 
Variables belonging to register storage class are local to the block which they are defined in,
and get destroyed on exit from the block.


ALL varaibles in C normallly impliitily defined  as auto...store at stack....
EXTERN -global variable.
.The main purpose of using extern variables is that they can be accessed between two different files 
which are part of a large program.


Dynamic memory allocation in C
malloc()----single large block of memory for eg int* ptr=(int*) malloc(20bytes);|  20 bytes    |  
calloc ----contigious allocation of memory for eg int* arr=(int*) calloc(5*sizeOf(int));   | | | | | | 5 blocks of 4 bytes
realloc---to increase the previous alloted memory for above we define ptr and now we want to increase its memory 
ptr=realloc(ptr,newSize);


Operating sysytem,C++,java,computer Networks................................................................


Find the number of sub-strings in a given string where each sub-string has the same character in beginning and end
Method 3 (Best approach) : Now if we carefully observe then we can realize that the answer just depends on frequencies of characters in the original string. For example in string abcab, frequency of ‘a’ is 2 and substrings contributing to answer are a, abca and a respectively, a total of 3, which is calculated by (frequency of ‘a’+1)C2.
filter_none
edit
play_arrow

brightness_4
// Most efficient C++ program to count all   
// substrings with same first and last characters. 
#include <bits/stdc++.h> 
using namespace std; 
const int MAX_CHAR = 26;  // assuming lower case only 
  
int countSubstringWithEqualEnds(string s) 
{ 
    int result = 0; 
    int n = s.length(); 
  
    // Calculating frequency of each character 
    // in the string. 
    int count[MAX_CHAR] = {0}; 
    for (int i=0; i<n; i++) 
        count[s[i]-'a']++; 
  
    // Computing result using counts 
    for (int i=0; i<MAX_CHAR; i++) 
        result += (count[i]*(count[i]+1)/2); 
  
    return result; 
} 
  
// Driver function 
int main() 
{ 
    string s("abcab"); 
    cout << countSubstringWithEqualEnds(s); 
    return 0; 
} 





Finf sum of  longest path from root to leaf node?.
using namespace std; 
  
// Node of a binary tree 
struct Node { 
    int data; 
    Node* left, *right; 
}; 
  
// function to get a new node 
Node* getNode(int data) 
{ 
    // allocate memory for the node 
    Node* newNode = (Node*)malloc(sizeof(Node)); 
  
    // put in the data 
    newNode->data = data; 
    newNode->left = newNode->right = NULL; 
    return newNode; 
} 
  
// function to find the sum of nodes on the 
// longest path from root to leaf node 
void sumOfLongRootToLeafPath(Node* root, int sum, 
                      int len, int& maxLen, int& maxSum) 
{ 
    // if true, then we have traversed a 
    // root to leaf path 
    if (!root) { 
        // update maximum length and maximum sum 
        // according to the given conditions 
        if (maxLen < len) { 
            maxLen = len; 
            maxSum = sum; 
        } else if (maxLen == len && maxSum < sum) 
            maxSum = sum; 
        return; 
    } 
  
    // recur for left subtree 
    sumOfLongRootToLeafPath(root->left, sum + root->data, 
                            len + 1, maxLen, maxSum); 
  
    // recur for right subtree 
    sumOfLongRootToLeafPath(root->right, sum + root->data, 
                            len + 1, maxLen, maxSum); 
} 
  
// utility function to find the sum of nodes on 
// the longest path from root to leaf node 
int sumOfLongRootToLeafPathUtil(Node* root) 
{ 
    // if tree is NULL, then sum is 0 
    if (!root) 
        return 0; 
  
    int maxSum = INT_MIN, maxLen = 0; 
  
    // finding the maximum sum 'maxSum' for the 
    // maximum length root to leaf path 
    sumOfLongRootToLeafPath(root, 0, 0, maxLen, maxSum); 
  
    // required maximum sum 
    return maxSum; 
} 
  
// Driver program to test above 
int main() 
{ 
    // binary tree formation 
    Node* root = getNode(4);         /*        4        */
    root->left = getNode(2);         /*       / \       */
    root->right = getNode(5);        /*      2   5      */
    root->left->left = getNode(7);   /*     / \ / \     */
    root->left->right = getNode(1);  /*    7  1 2  3    */
    root->right->left = getNode(2);  /*      /          */
    root->right->right = getNode(3); /*     6           */
    root->left->right->left = getNode(6); 
  
    cout << "Sum = "
         << sumOfLongRootToLeafPathUtil(root); 
  
    return 0; 
} 

 
 
 Reverse individual words with O(1) extra space??
 string reverseWords(string str) 
{ 
  
    // Pointer to the first character 
    // of the first word 
    int start = 0; 
    for (int i = 0; i <= str.size(); i++) { 
  
        // If the current word has ended 
        if (str[i] == ' ' || i == str.size()) { 
  
            // Pointer to the last character 
            // of the current word 
            int end = i - 1; 
  
            // Reverse the current word 
            while (start < end) { 
                swap(str[start], str[end]); 
                start++; 
                end--; 
            } 
  
            // Pointer to the first character 
            // of the next word 
            start = i + 1; 
        } 
    } 
  
    return str; 
} 



. Fractional knapsack and implementing it using dynamic programming ( modify 01 knapsack).??
using namespace std; 
  
// Structure for an item which stores weight and corresponding 
// value of Item 
struct Item 
{ 
    int value, weight; 
  
    // Constructor 
    Item(int value, int weight) : value(value), weight(weight) 
    {} 
}; 
  
// Comparison function to sort Item according to val/weight ratio 
bool cmp(struct Item a, struct Item b) 
{ 
    double r1 = (double)a.value / a.weight; 
    double r2 = (double)b.value / b.weight; 
    return r1 > r2; 
} 
  
// Main greedy function to solve problem 
double fractionalKnapsack(int W, struct Item arr[], int n) 
{ 
    //    sorting Item on basis of ratio 
    sort(arr, arr + n, cmp); 
  
    //    Uncomment to see new order of Items with their ratio 
    /* 
    for (int i = 0; i < n; i++) 
    { 
        cout << arr[i].value << "  " << arr[i].weight << " : " 
             << ((double)arr[i].value / arr[i].weight) << endl; 
    } 
    */
  
    int curWeight = 0;  // Current weight in knapsack 
    double finalvalue = 0.0; // Result (value in Knapsack) 
  
    // Looping through all Items 
    for (int i = 0; i < n; i++) 
    { 
        // If adding Item won't overflow, add it completely 
        if (curWeight + arr[i].weight <= W) 
        { 
            curWeight += arr[i].weight; 
            finalvalue += arr[i].value; 
        } 
  
        // If we can't add current Item, add fractional part of it 
        else
        { 
            int remain = W - curWeight; 
            finalvalue += arr[i].value * ((double) remain / arr[i].weight); 
            break; 
        } 
    } 
  
    // Returning final value 
    return finalvalue; 
}




Longest palindromic substring

 int longestPalSubstr(string str) 
{ 
    // get length of input string 
    int n = str.size();  
  
    // table[i][j] will be false if substring str[i..j] 
    // is not palindrome. 
    // Else table[i][j] will be true 
    bool table[n][n]; 
      
    memset(table, 0, sizeof(table)); 
  
    // All substrings of length 1 are palindromes 
    int maxLength = 1; 
      
    for (int i = 0; i < n; ++i) 
        table[i][i] = true; 
  
    // check for sub-string of length 2. 
    int start = 0; 
    for (int i = 0; i < n-1; ++i) 
    { 
        if (str[i] == str[i+1]) 
        { 
            table[i][i+1] = true; 
            start = i; 
            maxLength = 2; 
        } 
    } 
  
    // Check for lengths greater than 2. k is length 
    // of substring 
    for (int k = 3; k <= n; ++k) 
    { 
        // Fix the starting index 
        for (int i = 0; i < n-k+1 ; ++i) 
        { 
            // Get the ending index of substring from 
            // starting index i and length k 
            int j = i + k - 1; 
  
            // checking for sub-string from ith index to 
            // jth index iff str[i+1] to str[j-1] is a 
            // palindrome 
            if (table[i+1][j-1] && str[i] == str[j]) 
            { 
                table[i][j] = true; 
  
                if (k > maxLength) 
                { 
                    start = i; 
                    maxLength = k; 
                } 
            } 
        } 
    } 
  
   cout << "Longest palindrome substring is: "; 
   printSubStr( str, start, start + maxLength - 1 ); 
      
    // return length of LPS 
    return maxLength; 
} 

Application of DFS and BFS.
1) Shortest Path and Minimum Spanning Tree for unweighted graph In an unweighted graph, the shortest path is the path with least 
number of edges. With Breadth First, we always reach a vertex from given source using the minimum number of edges.
Also, in case of unweighted graphs, any spanning tree is Minimum Spanning Tree and we can use either Depth or Breadth first 
traversal for finding a spanning tree.

2) Peer to Peer Networks. In Peer to Peer Networks like BitTorrent, Breadth First Search is used to find all neighbor nodes.

3) Crawlers in Search Engines: Crawlers build index using Breadth First. The idea is to start from source page and follow all
links from source and keep doing same. Depth First Traversal can also be used for crawlers, but the advantage with Breadth First
Traversal is, depth or levels of the built tree can be limited.

4) Social Networking Websites: In social networks, we can find people within a given distance ‘k’ from a person using Breadth
First Search till ‘k’ levels.

5) GPS Navigation systems: Breadth First Search is used to find all neighboring locations.

6) Broadcasting in Network: In networks, a broadcasted packet follows Breadth First Search to reach all nodes.

7) In Garbage Collection: Breadth First Search is used in copying garbage collection using Cheney’s algorithm. Refer this and for
details. Breadth First Search is preferred over Depth First Search because of better locality of reference:

8) Cycle detection in undirected graph: In undirected graphs, either Breadth First Search or Depth First Search can be used to
detect cycle. In directed graph, only depth first search can be used.

9) Ford–Fulkerson algorithm In Ford-Fulkerson algorithm, we can either use Breadth First or Depth First Traversal to find the
maximum flow. Breadth First Traversal is preferred as it reduces worst case time complexity to O(VE2).

10) To test if a graph is Bipartite We can either use Breadth First or Depth First Traversal.

11) Path Finding We can either use Breadth First or Depth First Traversal to find if there is a path between two vertices.

12) Finding all nodes within one connected component: We can either use Breadth First or Depth First Traversal to find all nodes
reachable from a given node.

Many algorithms like Prim’s Minimum Spanning Tree and Dijkstra’s Single Source Shortest Path use structure similar to Breadth
First Search.


os questions 
What is the difference between Mutex and Binary Semaphore though they work same?
mutex is a locking mechanaism and semphaphore is a signalling mechansim

What is difference between MAC address and IP address?
48 bits mac and 32 bits IP
mac is on NIC card,.IP is assigned by ISP
ARP retrieve MAc and RARP retrieve IP.




Difference between hub, switch and routers?
hub braodcast message Layer 1 of OSI
switch send data to specific location layer 2 off OSI
Router is used to connect two networks layer 3 of OSI






what isDHCP?
A DHCP server enables computers to request IP addresses 
and networking parameters automatically from the Internet service provider 





What is piggybacking?
In two-way communication, wherever a frame is received, the receiver waits and does not send the control frame (acknowledgement or ACK) back to the sender immediately.

The receiver waits until its network layer passes in the next data packet. The delayed acknowledgement is then attached to this outgoing data frame.

This technique of temporarily delaying the acknowledgement so that it can be hooked with next outgoing data frame is known as piggybacking.


What is flooding in routers?
Flooding is used in computer networks routing algorithm in which every incoming packet is sent through every outgoing link except the one it arrived on




Explain 3 way handshake connection establishment process in TCP?
TCP 3-way handshake

To establish a connection, TCP uses a three-way handshake. Before a client attempts to connect with a server, the server must 
first bind to and listen at a port to open it up for connections: this is called a passive open. Once the passive open is 
established, a client may initiate an active open. To establish a connection, the three-way (or 3-step) handshake occurs:

SYN(sequence number): The active open is performed by the client sending a SYN to the server. The client sets the segment's sequence number to
a random value A.
SYN-ACK: In response, the server replies with a SYN-ACK. The acknowledgment number is set to one more than the received
sequence number i.e. A+1, and the sequence number that the server chooses for the packet is another random number, B.
ACK: Finally, the client sends an ACK back to the server. The sequence number is set to the received acknowledgement value 
i.e. A+1, and the acknowledgement number is set to one more than the received sequence number i.e. B+1.
At this point, both the client and server have received an acknowledgment of the connection. The steps 1, 2 establish the 
onnection parameter (sequence number) for one direction and it is acknowledged. The steps 2, 3 establish the connection 
parameter (sequence number) for the other direction and it is acknowledged. With these, a full-duplex communication is 
established.

Number of subarrays having sum exactly equal to k?
// with sum exactly equal to k. 
#include <bits/stdc++.h> 
using namespace std; 
  
// Function to find number of subarrays  
// with sum exactly equal to k. 
int findSubarraySum(int arr[], int n, int sum) 
{ 
    // STL map to store number of subarrays 
    // starting from index zero having  
    // particular value of sum. 
    unordered_map<int, int> prevSum; 
  
    int res = 0; 
  
    // Sum of elements so far. 
    int currsum = 0; 
  
    for (int i = 0; i < n; i++) { 
  
        // Add current element to sum so far. 
        currsum += arr[i]; 
  
        // If currsum is equal to desired sum, 
        // then a new subarray is found. So 
        // increase count of subarrays. 
        if (currsum == sum)  
            res++;         
  
        // currsum exceeds given sum by currsum  
        //  - sum. Find number of subarrays having  
        // this sum and exclude those subarrays 
        // from currsum by increasing count by  
        // same amount. 
        if (prevSum.find(currsum - sum) !=  
                                  prevSum.end())  
            res += (prevSum[currsum - sum]); 
          
  
        // Add currsum value to count of  
        // different values of sum. 
        prevSum[currsum]++; 
    } 
  
    return res; 
} 
  
int main() 
{ 
    int arr[] = { 10, 2, -2, -20, 10 }; 
    int sum = -10; 
    int n = sizeof(arr) / sizeof(arr[0]); 
    cout << findSubarraySum(arr, n, sum); 
    return 0; 
} 


string matching ALGO KMP ???
#include <bits/stdc++.h> 
  
void computeLPSArray(char* pat, int M, int* lps); 
  
// Prints occurrences of txt[] in pat[] 
void KMPSearch(char* pat, char* txt) 
{ 
    int M = strlen(pat); 
    int N = strlen(txt); 
  
    // create lps[] that will hold the longest prefix suffix 
    // values for pattern 
    int lps[M]; 
  
    // Preprocess the pattern (calculate lps[] array) 
    computeLPSArray(pat, M, lps); 
  
    int i = 0; // index for txt[] 
    int j = 0; // index for pat[] 
    while (i < N) { 
        if (pat[j] == txt[i]) { 
            j++; 
            i++; 
        } 
  
        if (j == M) { 
            printf("Found pattern at index %d ", i - j); 
            j = lps[j - 1]; 
        } 
  
        // mismatch after j matches 
        else if (i < N && pat[j] != txt[i]) { 
            // Do not match lps[0..lps[j-1]] characters, 
            // they will match anyway 
            if (j != 0) 
                j = lps[j - 1]; 
            else
                i = i + 1; 
        } 
    } 
} 
  
// Fills lps[] for given patttern pat[0..M-1] 
void computeLPSArray(char* pat, int M, int* lps) 
{ 
    // length of the previous longest prefix suffix 
    int len = 0; 
  
    lps[0] = 0; // lps[0] is always 0 
  
    // the loop calculates lps[i] for i = 1 to M-1 
    int i = 1; 
    while (i < M) { 
        if (pat[i] == pat[len]) { 
            len++; 
            lps[i] = len; 
            i++; 
        } 
        else // (pat[i] != pat[len]) 
        { 
            // This is tricky. Consider the example. 
            // AAACAAAA and i = 7. The idea is similar 
            // to search step. 
            if (len != 0) { 
                len = lps[len - 1]; 
  
                // Also, note that we do not increment 
                // i here 
            } 
            else // if (len == 0) 
            { 
                lps[i] = 0; 
                i++; 
            } 
        } 
    } 
} 
  
// Driver program to test above function 
int main() 
{ 
    char txt[] = "ABABDABACDABABCABAB"; 
    char pat[] = "ABABCABAB"; 
    KMPSearch(pat, txt); 
    return 0; 
}





