[pseudocode.MD](https://github.com/user-attachments/files/32668655/pseudocode.MD)
CLASS Queue
     int FRONT = -1
     int REAR = -1
     ARRAY queue[SIZE]

Procedure enqueue(students)
IF REAR == SIZE - 1 THEN
PRINT "Queue is full"
   FRONT = 0
   REAR = 0
Else
   REAR = REAR + 1
   queue[rear] = student
ENDIF
End Procedure

Procedure dequeue()
    IF FRONT == -1 THEN
        PRINT "Queue is empty"
        Return NULL
    ELSE
         student = queue[front]
         IF FRONT = rear THEN
            FRONT = -1
            REAR = -1
        ELSE    
            FRONT == Front + 1
        ENDIF
         Return student
End Procedure
END Class           
  
   # STACK (push,pop,peek) 

CLASS Stack
int top = -1
ARRAY stackArray[100]

Procedure push(value)
    IF top < 99 THEN
       top = top + 1
       stackArray[top] = value
   Else
       Print "Stack overflow"
   End if
End Procedure

Function pop()
    IF top >= 0 THEN
        value = stackArray[top]
        top = top - 1
        RETURN value
   Else
        Print "Stack underflow" 
        Return NULL
   End if
End Function

Function peek()
    IF top >= 0 THEN 1
        Return stackArray[top]
   End if
   Return NULL
End Function
END Class

Function evaluatePostfix(expression)
   CREATE Stack

    FOR EACH symbol IN expression
        IF symbol IS a number THEN
            stack.push(symbol)
        ELSE  
            num2= stack.pop()
            num1= stack.pop()
            result = num1 symbol num2
            stack.push(result)
        END IF
    END FOR
    RETURN stack.pop()  
END Function

# SINGLY LINKED LISTS

CLASS singlylinkedlist
    StudentNode HEAD = NULL
    Insert at end
    Procedure insertNode(student)
       CREATE newNode WITH student
       IF HEAD == NULL THEN
          HEAD = newNode
      ELSE
          current = HEAD
          While current.Next != Null DO
                current = current.NEXT
         END While
         current.Next = newNode
      End IF
End Procedure

Procedure insertAtBeginning(student)
       CREATE newNode WITH student
       newNode.NEXT = HEAD
       HEAD = newNode
End Procedure       

PROCEDURE deleteNode(studentNumber)
    IF HEAD = NULL THEN RETURN END IF
    
   IF HEAD.studentNumber == studentNumber THEN
      HEAD = HEAD.NEXT
      RETURN
   END IF

   current = HEAD
   WHILE current.NEXT != NULL AND current.NEXT.studentNumber != studentNumber DO
         current= current.NEXT
   END WHILE

   IF current.NEXT != NULL THEN
      current.NEXT = current.NEXT.NEXT
   END IF         
END PROCEDURE

FUNCTION searchNode(studentNumber)
    current = HEAD
    WHILE current != NULL DO
        IF current.studentNumber = studentNumber THEN
            RETURN current
        END IF
        current = current.NEXT
    END WHILE
    RETURN NULL   
END PROCEDURE
  
   Traverse(Print All)
PROCEDURE traverseList()
    current = head
    WHILE current != NULL
        PRINT current.studentNumber, current.name
        current = current.NEXT
    END WHILE
END PROCEDURE

# Sorting Algorithms

Selection Sort
PROCEDURE selectionSort(array,n)
   FOR i = 0 TO n-2 DO
       minIndex = i
       FOR j = i + 1 to n-1 DO
           IF array[j] < array[minIndex] THEN
               minIndex = j
            End IF
      END FOR
      SWAP array[i] WITH array[minIndex]         
   END FOR
END PROCEDURE

Insertion Sort
Procedure insertionSort(array,n)
    FOR i = 1 to n-1 DO
    key = array[i]
    j= i - 1
    WHILE j >= 0 AND array[j] > key DO
          array[j + 1] = array[j]
          j=j-1
   END WHILE
   array[j + 1] = key
 END FOR
END Procedure

MERGE SORT
Procedure mergeSort(array,left,right)
   IF left < right THEN
       mid = (left + right)/2
       mergeSort(array,left,mid)
       mergeSort(array,mid + 1,right)
       merge(array,left,mid,right)
   END IF
  END Procedure

Quick Sort
Procedure quickSort(array,low,high)
   IF low < high THEN 
       pivotIndex = partition (array,low,high)
       quickSort(array,low,pivotIndex - 1)
       quickSort(array, pivotIndex + 1,high)
   END IF
END Procedure

