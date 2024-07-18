# c-codePractice-


## 1. Write a program, which reads from the console N integers and prints them in //reversed order. Use the Stack<int> class.

```c#
using System;
using System.Collections.Generic;

public class HelloWorld

{
    public Stack<int> ReadNintegers(Stack<int> stack)
    {
         
        
        Console.WriteLine ("enter the count of integers");
        int n= int.Parse(Console.ReadLine());
        for(int i=0;i<n;i++)
        {
            int m= int.Parse(Console.ReadLine());
            stack.Push(m);
        }
        return stack;
    }
   
    
    public static void Main(string[] args)
    {
        HelloWorld h = new HelloWorld();
        Stack<int> s = new Stack<int>();
        h.ReadNintegers(s);
        foreach(int i in s)
        {
            Console.WriteLine(i);
        }
        
    }
}
```


 ## Write a program that reads from the console a sequence of positive integer numbers. The sequence ends when an empty line is entered. Print the sequence sorted in ascending order.  

```C#
using System;
using System.Collections.Generic;

public class HelloWorld

{
    public List<int> ReadNintegers(List<int> list)
    {
        while(true)
        {
        string n= Console.ReadLine();
        if(string.IsNullOrWhiteSpace(n))
        {
            break;
        }
        else if (int.TryParse(n, out int a) )
        {
            list.Add(a);
        }
        else
        Console.WriteLine ("re-enter");     
        }
        return  list;
    }
    
    public void SortAsc(List<int> list)
    {
        list.Sort();
    }
   
    
    public static void Main(string[] args)
    {
        HelloWorld h = new HelloWorld();
        List<int> l = new List<int>();
        h.ReadNintegers(l);
        h.SortAsc(l);
        foreach(int i in l)
        {
            Console.WriteLine(i);
        }
        
    }
}
```
