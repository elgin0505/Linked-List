# Linked-List

1.Insert at Front 

Purpose: 
Insert a new node at the beginning of the linked list. 
Code: 
void insertFront(int value) { 
Node* newNode = new Node(value); 
newNode->next = head; 
head = newNode; 
} 
Line-by-Line Explanation: 
1. Create a new node dynamically. 
2. Connect the new node to the current head. 
3. Update head so the new node becomes the first node. 
Visualization: 
Initial: 
HEAD 
↓ 
[20] → [30] → [40] → NULL 
Create: 
newNode 
↓ 
[10] 
Connect: 
[10] ■■■■■■■■■■■■■■■→ [20] → [30] → [40] 
Move Head: 
HEAD 
↓ 
[10]→ [20] → [30] → [40] → NULL







2.Insert at End 

Purpose: 
Insert a node at the end of the linked list. 
Visualization: 
HEAD 
↓ 
[10] → [20] → [30] → NULL 
Traversal: 
current = 10 
current = 20 
current = 30 
Create: 
[40] → NULL 
Attach: 
HEAD 
↓ 
[10] → [20] → [30] → [40] → NULL 
Time Complexity: O(n)




3.Insert in Sorted Order 

Purpose: 
Maintain ascending order while inserting. 
Example: Insert 30 
Before: 
HEAD 
↓ 
[10] → [20] → [40] → [50] 
Comparison Process: 
10 < 30 ✓ 
20 < 30 ✓ 
40 > 30 STOP 
Reconnect: 
[20] → [30] → [40] 
Result: 
HEAD 
↓ 
[10] → [20] → [30] → [40] → [50] 
Time Complexity: O(n)






4.Delete a Node 

Purpose: 
Remove a node containing a specified value. 
Delete: 30 
Before: 
HEAD 
↓ 
[10] → [20] → [30] → [40] 
current stops at: 
[20] 
temp points to: 
[30] 
Reconnect: 
[20] ■■■■■■■■■■■→ [40] 
Delete temp 
Result: 
HEAD 
↓ 
[10] → [20] → [40] 
Time Complexity: O(n)


5.Search Operation 

Purpose: 
Find whether a value exists. 
Search for 40 
10 == 40 ? No 
20 == 40 ? No 
30 == 40 ? No 
40 == 40 ? Yes 
Return: 
true 
Time Complexity: O(n)
