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







