# singly-linked-lists
singly-linked-lists

In a nutshell, a SLL is a data struction that contains a head, tail and a length property.  SLL consists of nodes, and each node has a value and a pointer to another node or null.  Think of a set of train box-cars. 

SLL are fast for inserting and deleting data. This is because they don't have to re-index anything.  But because they don't have indexes, they don't offer random access.


### Basic code structure of a SLL

```
class Node {
  constructor(val){
    this.val = val;
    this.next = val;
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
    }
  }
}

var list = new singlyLinkedList()
list.push("High")
list.push("there")

```