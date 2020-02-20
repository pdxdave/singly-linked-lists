# singly-linked-lists
singly-linked-lists

In a nutshell, a SLL is a data struction that contains a head, tail and a length property.  SLL consists of nodes, and each node has a value and a pointer to another node or null.  Think of a set of train box-cars. 

Best use case:  SLL are fast for inserting and deleting data. This is because they don't have to re-index anything.  But because they don't have indexes, they don't offer random access.



### PUSH code

```
* set the intitial class.  

class Node {
  constructor(val){
    this.val = val;
    this.next = null;
  }
}

* SLL. We don't know the length, and in the beginning there is no head or tail.

class singlyLinkedList{
  
   constructor(){
    this.length = 0;
    this.head = null;
    this.tail = null;
  }
  
  push(val){
    var newNode = new Node(val)
    if(!this.head){
      this.head = newNode;
      this.tail = this.head;
    } else {
      this.tail.next = newNode;
      this.tail = newNode; // this is the new tail
  }
  this.length ++
  return this;  // returns list
 }
}

var list = new singlyLinkedList()
list.push("High")
list.push("there")

```

### POP code

Removes the tail node

* The trick is that we have to find the second to last item
* We have to be able to traverse the code

```

class Node {
  constructor(val){
    this.val = val;
    this.next = null;
  }
}


class singlyLinkedList{
  
   constructor(){
    this.length = 0;
    this.head = null;
    this.tail = null;
  }
  
  push(val){
    var newNode = new Node(val)
    if(!this.head){
      this.head = newNode;
      this.tail = this.head;
    } else {
      this.tail.next = newNode;
      this.tail = newNode;
  }
  this.length ++
  return this;  // returns list
 }
 pop(){
    if(!this.head) return undefined;
    var current = this.head;
    var newTail = current;
    while(current.next){
      newtail = current;
      current = current.next
    }
    this.tail = newTail;
    this.tail.next = null;
    this.length --;
    if(this.length === 0){
      this.head = null;
      this.tail = null;
    }
    return current;
  }
}

var list = new singlyLinkedList()
list.push("High")
list.push("there")
list.pop()

```

### SHIFT code

* removes the first item in the list


```
* set the intitial class.  

class Node {
  constructor(val){
    this.val = val;
    this.next = null;
  }
}

* SLL. We don't know the length, and in the beginning there is no head or tail.

class singlyLinkedList{
  
   constructor(){
    this.length = 0;
    this.head = null;
    this.tail = null;
  }
  
  push(val){
    var newNode = new Node(val)
    if(!this.head){
      this.head = newNode;
      this.tail = this.head;
    } else {
      this.tail.next = newNode;
      this.tail = newNode; // this is the new tail
  }
  this.length ++
  return this;  // returns list
 }
 
 shift(){
    if(!this.head) return undefined
    var currentHead = this.head;
    this.head = currentHead.next
    this.length --;
    return currentHead;
  } // end of shift
}

var list = new singlyLinkedList()
list.push("High")
list.push("there")
list.shift()

```

### UNSHIFT

* adds an item to the beginning of the list
```
class Node {
  constructor(val){
    this.val = val;
    this.next = null;
  }
}

class singlyLinkedList{
  
   constructor(){
    this.length = 0;
    this.head = null;
    this.tail = null;
  }
  
  push(val){
    var newNode = new Node(val)
    if(!this.head){
      this.head = newNode;
      this.tail = this.head;
    } else {
      this.tail.next = newNode;
      this.tail = newNode; // this is the new tail
  }
  this.length ++
  return this;  // returns list
 }
 
unshift(){
    let newNode = new Node(val)
    if(!this.head){
      this.head = newNode;
      this.tail = this.head;
    } else {
    newNode.next = this.head;
    this.head = newNode
    }
    this.length ++;
    return this
  }// end of unshift. adds new item to beginning of list
}

var list = new singlyLinkedList()
list.push("High")
list.push("there")
list.unshift("First")

```








