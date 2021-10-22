<<<<<<< HEAD
````javascript
import aaz.libquickjs;

// 创建运行时
var runtime = aaz.libquickjs.newRuntime();
// 在运行时创建上下文
var context = runtime.newContext();

// 测试非引用类型
assert( context.eval( `true` ).parseValue() === true, "布尔不通过"  )
assert( context.eval( `"a"` ).parseValue() === "a", "字符不通过"  )
assert( context.eval( `1` ).parseValue() === 1 , "整数不通过" )
assert( context.eval( "0.1" ).parseValue() === 0.1, "浮点不通过" )


// 测试引用类型，返回一个对象，引用类型用完要手动释放
var code = /**
(()=>{return {abc:2};})()
**/

var v = context.eval(code)
v.parseValue()
v.free()
````
=======
# quickjs-aardio
aardio
>>>>>>> beba7fbab937beaffc5a268ed5be02eabef68751
