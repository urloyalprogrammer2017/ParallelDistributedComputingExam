# ParallelDistributedComputingExam
#LEVEL 5 Source Code/Output Screenshot

Task
1. Flatten the given Linked list Sorting must be performed during the flattening of the linked list

Answer: Source Code


# Programmed by: Luganob Jerald M. BSCS-3B

class Node:
    def __init__(self, data):
        self.data = data;
        self.next = None;

    def print_nodes(self):
        current = self
        while current:
            print(f"{current.data}")
            current = current.next


class SortList:
    # Represent the head and tail of the singly linked list
    def __init__(self):
        self.head = None;
        self.tail = None;

        # addNode() will add a new node to the list

    def addNode(self, data):
        # Create a new node
        newNode = Node(data);

        # Checks if the list is empty
        if (self.head == None):
            # If list is empty, both head and tail will point to new node
            self.head = newNode;
            self.tail = newNode;
        else:
            # newNode will be added after tail such that tail's next will point to newNode
            self.tail.next = newNode;
            # newNode will become new tail of the list
            self.tail = newNode;

            # sortList() will sort nodes of the list in ascending order

    def sortList(self):
        # Node current will point to head
        current = self.head;
        index = None;

        if (self.head == None):
            return;
        else:
            while (current != None):
                # Node index will point to node next to current
                index = current.next;

                while (index != None):
                    # If current node's data is greater than index's node data, swap the data between them
                    if (current.data > index.data):
                        temp = current.data;
                        current.data = index.data;
                        index.data = temp;
                    index = index.next;
                current = current.next;

                # display() will display all the nodes present in the list

    def display(self):
        # Node current will point to head
        current = self.head;
        if (self.head == None):
            print("List is empty");
            return;
        while (current != None):
            # Prints each node by incrementing pointer
            print(current.data),
            current = current.next;
        print
        ""



# Connect Node
# Head
node_10 = Node('10')
node_1 = Node('1')
node_3 = Node('3')
node_9 = Node('9')

# connect head
node_10.next = node_1
node_1.next = node_3
node_3.next = node_9
pheadnode = node_10
print("Head Node:")
pheadnode.print_nodes()

# right Node 1
node_1.next = node_3
node_3.next = node_9
rnode1 = node_1
print("\nright nodes 1:")
rnode1.print_nodes()

#right node 3
node_3.next = node_9
rnode3 = node_9
print("\nRight node 3:")
rnode3.print_nodes()

# number 1 nodes
node_8 = Node('8')
node_6 = Node('6')
node_2 = Node('2') # right node of 6

# connect bottom node 1
node_8.next = node_6
n1bttmnodes = node_8
print("\nBottom nodes 1:")
n1bttmnodes.print_nodes()

# node 6 left node
node_6.next = node_2 # left Node
rnode = node_2

print("\nLeft node 6:")
rnode.print_nodes()

# 3 Up node
node_7 = Node('7') # Up node
node_3.next = node_7
nodeup3 = node_7
print("\nUp node 3:")
nodeup3.print_nodes()

# 3 bottom node
node_4 = Node('4') # Bottom node
node_5 = Node('5') # Right node
node_3.next = node_4
bttmnode3 = node_4
print("\nBottom node 3:")
bttmnode3.print_nodes()

node_4.next = node_5
rnode4 = node_5
print("\nRight node 4:")
rnode4.print_nodes()

sList = SortList();
# Adds data to the list
sList.addNode(10);
sList.addNode(1);
sList.addNode(3);
sList.addNode(9);

# 1 Bottom node
sList.addNode(8)
sList.addNode(6)
sList.addNode(2) # Left 6 node

#3 up and down node
sList.addNode(7) # Up Node
sList.addNode(4) # Bottom Node
sList.addNode(5) # 4 Right Node
sList.sortList();


# Displaying sorted list
print("\nSorted list: ");
sList.display();


![2](https://user-images.githubusercontent.com/89097911/181264991-63cde0ed-40f5-4920-9bfe-f5d4ed425972.png)
![level5](https://user-images.githubusercontent.com/89097911/181264994-ec774f0f-21d2-40f3-aa64-363d99bda6d9.png)

