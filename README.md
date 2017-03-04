
**1.** 有一个长度未知的数组a，如果它的长度为0就把数字1添加到数组里面，否则按照先进先出的队列规则让第一个元素出队
```javascript
a.length === 0 ? a.push(1) : a.shift();
```
**2.** console.log('hello'.repeatify(3))期望打印出hellohellohello
```javascript
String.prototype.repeatify = function(arg) {
   var temp = '';
   for (var i = 0; i < arg; i++) {
      temp += this;
   }
   return temp;
};
```
**3.** 下面代码如何改可以让person()打印出Colin Ihrig

```javascript
	var fullname = 'John Doe'
	var obj = {
		fullname: 'Colin Ihrig',
		getFullname: function() {
		return this.fullname
		}
	}
	var person = obj.getFullname
	console.log(obj.getFullname()) // Colin Ihrig
	console.log(person()) // John Doe
		
    console.log(person.call(obj));//用call改变this指向
```

**4.** 不使用loop循环，创建一个长度为100的数组，并且每个元素的值等于它的下标
```javascript
Object.keys(Array.apply(null,{length:100}));
//{length:100}是由于有length属性，被当做类数组对象,其中每个元素都是undefined
//Array.apply(null,{length:100}就相当于Array{undefined,undefined,undefined...}
//即创建了100个值为undefined元素的数组
//Object.keys()方法参数为数组时，返回索引组成的数组
```

**5.**  上机题答案是同一个仓库的其他所有文件~