# IronPulse 6941 代码规范

## 命名
1. 类需要使用大驼峰命名，即 `UpperCamelCase`。
2. 方法名、参数名、成员变量、局部变量，使用小驼峰命名，即 `lowerCamelCase`。
3. 常量、枚举值需全部大写并在单词之间添加下划线，如 `THIS_IS_A_CONSTANT`。但如果常量类型不为基本类型，则采用小驼峰命名。
4. Subsystem 类后需要加上 Subsystem，如 `SwerveSubsystem`。
5. 布尔语义禁止采用 `isDeleted` 的形式，一律采用 `deleted`。
6. 接口类中的方法和属性不要加任何修饰符号 (`public` 也不要加)

## 格式
1. 在大括号之前必须添加空格，如 `public class ABC { ... }`。而不是 `public class ABC{ ... }`
2. 在 `if`、`for`、`while`、`switch` 等关键字与 `(` 之间同样需要添加空格，如 `if (xxx)`，而不是 `if(xxx)`
3. 对于过长的代码行，可以适当考虑进行换行。
4. 勤使用换行符分割代码片段。对于过于长的代码片段，可以考虑提取函数。
5. 禁止出现超过三层的嵌套语句。对于 `if` 条件控制，可以采用守卫模式，即反转布尔值以将操作从 `if` 当中提取出来。也可以考虑提前返回。

## 注释
1. 对于 `interface`，必须包含对其所有方法的 `JavaDoc` 注释。对于 `class`，`JavaDoc` 可选。
2. 尽量少添加行内注释。如果你觉得有必要添加，可以考虑适当修改代码逻辑使其更加清晰。

## 杂项
1. 对于可能为空的值，必须使用 `Optional<T>` 标识出来。
2. 对于单位不明的量，如 `double speed;`、`double periodTime;`，使用 WPILib 的 [Units](https://docs.wpilib.org/en/stable/docs/software/basic-programming/java-units.html) 库
