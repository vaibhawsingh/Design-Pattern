# Design Pattern
Design Pattern in c++

[1. Creational Patterns](#1-creational-patterns)

 - [1.1 Singleton](#1.1-singleton)
 - [1.2 Builder](#1.2-builder)

-----------------------------------------------------------------------------------------------------------------------------------
<!-- toc -->
## 1. Creational Patterns ##
 **Ceational design patterns** are design patterns that deal with object creation mechanisms.
### 1.1 Singleton
 A class of which only a single instance can exist. The **Singleton pattern** ensures that a class has only one instance and provides a global point of access to that instance. It is named after the singleton set, which is defined to be a set containing one element. This is useful when exactly one object is needed to coordinate actions across the system. 
### Ex:
<pre><code>
class SingleTon
{
public:
	static SingleTon* GetObj()
	{
		if (obj == nullptr)
			obj = new SingleTon;
		return obj;
	}
	void print()
	{
		cout << count << endl;
	}
private:
	static SingleTon *obj ;
	static int count;
	SingleTon(){}
};
int SingleTon::count = 0;
SingleTon *SingleTon::obj = nullptr;
int main()
{
	SingleTon *obj;
	obj = SingleTon::GetObj();
	obj->print();
	SingleTon *obj1;
	obj1 = SingleTon::GetObj();
	obj1->print();
	_getch();
	return 0;
}
</code></pre>

### 1.2 Builder Pattern
  Separates object construction from its representation. The **Builder Pattern** is used to separate the construction of a complex object from its representation so that the same construction process can create different objects representations.

