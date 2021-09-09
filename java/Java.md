#基础
##abstract
抽象类（abstract class ）
1.只要有个方法是abstract ，那么该类是abstract 类；
2.abstract 方法在子类中必须有实现；在abstract 类中的abstract 方法只有声明而不能有方法体；
3.abstract 方法在子类中被实现时要加上override关键字；
4.abstract 类方法中非abstract 方法在子类中重写时加上new关键字；

接口（ interface）
1.只有方法声明，实现类来实现方法；
2.成员变量是static和final的;

接口和抽象类（abstract class and interface） 不同点：
1.继承一个抽象类，继承多个接口
2.类里面只要有一个抽象方法，该类就是抽象类；
3.抽象类可以是抽象方法和普通方法，接口中的方法都是声明（只有方法名，没有内部实现），必须被继承