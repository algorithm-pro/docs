## 反转链表
Input: 1->2->3->4->5->NULL  
Output: 5->4->3->2->1->NULL

```
def reverseList(self, head):
    cur, prev = head, None
    while cur:
        cur.next, prev, cur = prev, cur, cur.next
    return prev
```

## 链表两两反转
Given 1->2->3->4 return 2->1->4->3
```
def swapPairs(self, head):
    pre, pre.next = self, head
    while pre.next and pre.next.next:
        a = pre.next
        b = a.next
        pre.next, b.next, a.next = b, a, b.next
        pre = a
    return self.next
```

## 判断链表有没有环  
用快慢指针处理
```
def hasCycle(self, head):
    fast = slow = head
    while slow and fast and fast.next:
        slow = slow.next
        fast = fast.next.next
        if slow is fast:
            return True
    return False
```

