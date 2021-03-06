# 制定代码审查标准的目的

* 代码审查的目的在于提高代码质量，帮助大家改善编码习惯，甚至提高大家的技术水平。
* 代码审查需要标准，否则大家没有方向，无法达到好的效果
* 审查标准需要集思广益，大家共同来完善和维护，最终形成适合我们自己的明确清晰的审查清单

# 代码审查中需要关注的内容

## 注释

* 每个类和方法都要有Javadoc，并且能明确表明类和方法的作用
* 代码中采用了一些技巧/捷径或者复杂的逻辑都要有注释说明
* 对打算后续重构或完善的代码应打上 TODO 之类的标记，便于编辑器快速定位

## 命名

* 类和方法都要使用驼峰命名法
* 包名要以倒置的产品域名开头，并按层级、上下文来进行分包
* 尽可能不要使用拼音或者难以理解的缩写，命名应使其他人能够快速理解

## 代码

* 代码应做基本的格式化，排版要整洁，方便他人可读
* 代码要容易理解，谁都能写出机器能读懂的代码，写出人能读懂的代码才是水平
* 重复使用的相同代码应提取成帮助类等形式，便于复用
* 避免创建过重的对象或方法（方法不应超过100行），对象和方法应符合单一职责原则
* 不使用的代码要删除
* 不要使用 System.out.println 打印日志，且应使用最合适的日志级别
* 不要使用 Exception.printStackTrace 打印异常，且对异常应作出合理的处理，不要只是打印就完事了，为何这么处理应注释说明
* 类不应有多个重载的构造方法，如果确实存在实例化时传入不同成员变量的需要，应使用静态工厂模式
* 方法应使用合理的访问控制，而不是所有的方法都写成 public 的
* 使用 Spring、Mybatis 等框架时，尽可能遵循最佳实践建议（最佳实践大家共同积累）
* 要有覆盖率较高的单元测试

## 设计

* 对象、变量的作用域是否合理
* 代码是否存在线程安全问题
* 代码是否符合面向对象的 S.O.L.I.D 原则
* 是否使用了合理的数据结构
