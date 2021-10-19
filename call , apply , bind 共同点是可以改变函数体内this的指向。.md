call , apply , bind 共同点是可以改变函数体内this的指向。

call 的调用对象必须是函数function，第一个参数是一个对象，第二个参数可以是任意个参数

调用apply的对象必须是函数function，第一个参数第对象，第二个参数必须是数组或类数组。类数组是不能使用foreach，splice，push等原型链上的方法。

function(){}.call({},...)

function(){}.apply({},[])

apply的第二个参数必须是数组或类数组。

合并两个数组，使用apply：Array . prototype.push . apply(数组名1，数组名2)  

Array.prototype.push.apply() 合并两个数组

获取数组中的最大值和最小值：

- Math . max . apply (Math , arr)
- Math . max . call (Math , ...arr)

遍历数组的方法：foreach , map , filter , for of , some , every , reduce

原型：

