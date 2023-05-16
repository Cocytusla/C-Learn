# C-Learn
数据类型
  枚举：整形常量的集合，可以自定义
  数组：任意变量类型顺序存储的数据
  结构体：任意变量的数据集合，可以自定义

枚举：一般用它来表示状态类型等
  申明枚举： 相当于是创建一个自定义的枚举类型
  申明枚举变量：使用申明的自定义枚举类型创建一个枚举变量

申明枚举语法：
  enum  E_自定义枚举名
  {
    自定义枚举项名字，//枚举中包裹的整形常量，第一个默认值是0，下面会一次累加
    自定义枚举项名字，
  }

申明枚举位置：
  1.namespace语句块中（常用）
  2.class语句块中 struct语句块中
  注意：枚举不能在函数语句块中申明

枚举使用：
//申明枚举变量
//自定义枚举类型 变量名=默认值；（自定义枚举类型.枚举项）
namespace Lesson_1枚举
{

    enum E_MonsterTpye
    {
        Norml,

        Boss,
    }

    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");

            E_MonsterTpye monsterTpye = E_MonsterTpye.Boss;
            //if (monsterTpye==E_MonsterTpye.Boss)
            //{
            //    Console.WriteLine("Boss逻辑");
            //}

            switch (monsterTpye)
            {
                case E_MonsterTpye.Norml:
                    //Console.WriteLine("普通怪");
                    //break;
                case E_MonsterTpye.Boss:
                    Console.WriteLine("BOSS怪");
                    break;
                default:
                    break;
            }
        }
    }
}

特征--成员变量

行为--成员方法

初始化调用--构造函数

释放时调用--析构函数

成员属性

索引器

静态成员

在C#中，静态类和静态构造函数是两个不同的概念。

静态类（Static Class）：

静态类是指只包含静态成员（静态字段、静态方法、静态属性）的类，不能被实例化。
静态类的成员可以通过类名直接访问，无需创建对象实例。
静态类常用于定义工具类、辅助类或者包含一些公用的静态方法和属性。
静态构造函数（Static Constructor）：

静态构造函数是一个特殊的构造函数，用于初始化静态成员。
静态构造函数在类第一次被使用之前自动调用，且只会被调用一次。
静态构造函数没有参数，没有访问修饰符，且无法被显式调用。
静态构造函数可以用来执行一些初始化操作，例如加载配置、初始化静态数据等。
以下是一个示例代码，演示了静态类和静态构造函数的使用：

csharp
Copy code
public static class MyStaticClass
{
    public static int MyStaticProperty { get; set; }

    public static void MyStaticMethod()
    {
        // 静态方法的实现
    }
}

public class MyClass
{
    static MyClass()
    {
        // 静态构造函数的实现
    }
}

// 使用静态类和静态构造函数
MyStaticClass.MyStaticProperty = 10;
MyStaticClass.MyStaticMethod();

MyClass myObj = new MyClass(); // 实例化 MyClass 类时，静态构造函数会被自动调用






