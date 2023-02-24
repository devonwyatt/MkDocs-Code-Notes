# Code

# **C#**
``` C#

```
``` C#
// EventHandlers
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Timers;
using System.Threading.Tasks;
using static System.Console;
using Timer = System.Timers.Timer;

namespace Events101
{
    class Program
    {
        static void Main(string[] args)
        {
            EventPublisher E = new EventPublisher();
            EventSubscriber S = new EventSubscriber();
            S.Subscribe();
            Timer timer = new Timer(1000);
            timer.Elapsed += (sender, e) => E.OnRaiseCustomEvent();
            timer.Start();
            WriteLine("Start");
                for (; ; )
                {
                    WriteLine("Hello world");
                    System.Threading.Thread.Sleep(1000);
                }
            }
        }
    

    class EventPublisher
    {
        static public event EventHandler RaiseCustomEvent;
        public void OnRaiseCustomEvent() => RaiseCustomEvent?.Invoke(this, new EventArgs());
    }
    class EventSubscriber
    {
        public void Subscribe() => EventPublisher.RaiseCustomEvent += MyEventHandler;
        public void Unsubscribe() => EventPublisher.RaiseCustomEvent -= MyEventHandler;
        public void MyEventHandler(object sender, EventArgs e) => WriteLine("Event received!");
    }
}

``` 
``` C#
public int String1 = 12;
``` 
``` C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Net.Http.Headers;
using System.Net.Security;
using System.Reflection.Emit;
using System.Runtime.CompilerServices;
namespace Steve
{
class MyClass
{
static void Main(string[] args)
{
Animal one = new Animal("Monkey", 2, "black", "");
Animal two = new Animal("Cat", 4, "red", "");
Animal three = new Animal("Dog", 4, "Green", "");
Animal Four = new Animal("Fish", 0, "blue", "");
pet P = new pet("Fish", "Yellow", 2);
Console.WriteLine(one);
Console.WriteLine(two);
Console.WriteLine(three);
Console.WriteLine(Four);
Console.WriteLine(P);
}
}

class Animal
{
public string name;
public string color;
public int Numboflegs { get;private set; }
public string label;

public Animal(string name, int Numboflegs, string color, string label)
{
this.name = name;
this.Numboflegs = Numboflegs;
this.color = color;
this.label = label;
}
public override string ToString()
{
if (Numboflegs == 2)
label = "Biped";
else if (Numboflegs == 4)
label = "Quadraped";
else label = "undefied";
return
$"The animal is a {this.name} and it has {this.Numboflegs} legs and it is {this.color} Which means it is a {this.label} ";
}
} 
class pet : Animal 
{
public string Name { get; set; }
public pet(string Name, string color, int Numboflegs) : base("",Numboflegs,color,"") {
this.Name = Name;
}

public override string ToString()
{ return $"{base.ToString()}called {Name}";}


}
List < student > = new List<students>();
students s;

s = new student("steve", new DateTime(2000, 2, 2));
students.Add(s);
foreach (student x in studenta) Wrtiteline(x)
``` 
```  C#

class myClass
{
    static void Main(string[] args)
    {


        List<student> students = new List<student>()
{
        new student("steve", new DateTime(2000, 2, 2)),
        new student("Jeff", new DateTime(2000, 3, 3)),
        new student("Sara", new DateTime(2001, 4, 4)),
        new student("Sarah", new DateTime(2003, 4, 4))
};
        students.Find((n) => n.name == "steve")?.withdrawStudent();

        foreach (student x in students.Where((n) => n.isactive)) { Console.WriteLine(x); }

        var sublist = students.Where(student => student.name == "steve");
        foreach (student x in sublist)
        { Console.WriteLine(x); }
        Console.WriteLine($"There are {student.Getnumbofstudents()} active students");
    } }



class person {
    public string name { get; set; }
    public DateTime dob { get;private set; }

    public person(string name, DateTime dob)
    {
        this.name = name;
        this.dob = dob;
    }

    public person(string name, int y, int m, int d) 
        : this(name, new DateTime(y, m, d)) 
    {
       
    }
    public override string ToString() => $"{name}";


}

class student : person
{
    static private int lastnumallocated = 0;
    static private int numberofstudents = 0;
    public bool isactive { get; set; }

    public string studnum { get; private set; }
    public student(string name, DateTime dob) : base(name, dob)
    {
        lastnumallocated++;
        numberofstudents++;
        isactive= true; 
        studnum = lastnumallocated.ToString();
    }
    public void withdrawStudent()
    {
        isactive= false;
        numberofstudents--;
    }

    static public int Getnumbofstudents() => numberofstudents;
    public override string ToString() => $"{base.ToString()} ({studnum})";
}


```

# **Python**

# **MKDocs**
