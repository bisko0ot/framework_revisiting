# framework_revisiting
JavaCollectionsProject/
│
├── src/
│   ├── KthSmallestElement.java
│   ├── WordFrequencyTreeMap.java
│   ├── PriorityQueueStack.java
│   ├── PriorityQueueQueue.java
│   ├── StudentTreeMap.java
│   ├── LinkedListEquality.java
│   └── EmployeeHashMap.java
│
└── README.md
import java.util.ArrayList;
import java.util.Collections;

public class KthSmallestElement {

    public static void main(String[] args) {

        // Creating ArrayList
        ArrayList<Integer> list = new ArrayList<>();
        list.add(20);
        list.add(5);
        list.add(15);
        list.add(10);
        list.add(30);

        int k = 3; // find 3rd smallest element

        // Sorting the ArrayList
        Collections.sort(list);

        // kth smallest element
        System.out.println("Kth Smallest Element: " + list.get(k - 1));
    }
}
import java.util.TreeMap;

public class WordFrequencyTreeMap {

    public static void main(String[] args) {

        String text = "java is easy and java is powerful";

        String[] words = text.split(" ");

        TreeMap<String, Integer> map = new TreeMap<>();

        for (String word : words) {
            map.put(word, map.getOrDefault(word, 0) + 1);
        }

        System.out.println("Word Frequencies:");
        System.out.println(map);
    }
}
import java.util.PriorityQueue;

public class PriorityQueueStack {

    static class StackNode {
        int value;
        int priority;

        StackNode(int value, int priority) {
            this.value = value;
            this.priority = priority;
        }
    }

    public static void main(String[] args) {

        PriorityQueue<StackNode> stack =
                new PriorityQueue<>((a, b) -> b.priority - a.priority);

        int priority = 0;

        stack.add(new StackNode(10, priority++));
        stack.add(new StackNode(20, priority++));
        stack.add(new StackNode(30, priority++));

        System.out.println("Stack Pop Order:");
        while (!stack.isEmpty()) {
            System.out.println(stack.poll().value);
        }
    }
}
import java.util.PriorityQueue;

public class PriorityQueueQueue {

    static class QueueNode {
        int value;
        int priority;

        QueueNode(int value, int priority) {
            this.value = value;
            this.priority = priority;
        }
    }

    public static void main(String[] args) {

        PriorityQueue<QueueNode> queue =
                new PriorityQueue<>((a, b) -> a.priority - b.priority);

        int priority = 0;

        queue.add(new QueueNode(10, priority++));
        queue.add(new QueueNode(20, priority++));
        queue.add(new QueueNode(30, priority++));

        System.out.println("Queue Poll Order:");
        while (!queue.isEmpty()) {
            System.out.println(queue.poll().value);
        }
    }
}
import java.util.TreeMap;

public class StudentTreeMap {

    public static void main(String[] args) {

        TreeMap<Integer, String> students = new TreeMap<>();

        students.put(101, "Sadia Afrose");
        students.put(102, "Rup Kumar");
        students.put(103, "Nusrat Jahan");

        System.out.println("Student Details:");
        for (var entry : students.entrySet()) {
            System.out.println(entry.getKey() + " -> " + entry.getValue());
        }
    }
}
import java.util.LinkedList;

public class LinkedListEquality {

    public static void main(String[] args) {

        LinkedList<Integer> list1 = new LinkedList<>();
        LinkedList<Integer> list2 = new LinkedList<>();

        list1.add(1);
        list1.add(2);
        list1.add(3);

        list2.add(1);
        list2.add(2);
        list2.add(3);

        if (list1.equals(list2)) {
            System.out.println("LinkedLists are equal");
        } else {
            System.out.println("LinkedLists are not equal");
        }
    }
}
import java.util.HashMap;

public class EmployeeHashMap {

    public static void main(String[] args) {

        HashMap<Integer, String> employees = new HashMap<>();

        employees.put(1001, "HR");
        employees.put(1002, "IT");
        employees.put(1003, "Finance");

        System.out.println("Employee Details:");
        System.out.println(employees);
    }
}
# Java Collections Framework Project

This project demonstrates the use of Java Collection Framework.
All programs are written inside the src directory with comments
and explanations.

Topics Covered:
- ArrayList
- TreeMap
- PriorityQueue
- LinkedList
- HashMap
