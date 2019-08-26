
##html5 localStorage对象操作

1. 在h5中 本地存储是一个window的属性 包括localStorage和sessionStorage 
2. 从名字应该可以很清楚的辨认二者区别，前者是一直存在在本地的，后者只是伴随着session
3. 窗口一旦关闭就没了，二者用法完全相同

		<script>
			// 验证浏览器时是否支持localStorage
			if(window.localStorage){
			    alert('支持')
			}else{
			    alert('不支持')
			}
		
		</script>

##h5 localStorage操作使用 三种设置本地存储的方法

1. localStorage.t1="张三"
2. localStorage['t2']='张三'
3. localStorage.setItem('t3','张三')


##三种访问本地存储的方法

1. localStorage.t1
2. localStorage['t2']
3. localStorage.getItem('t3')


		const TODOS_KEY = 'todos_key'
		export default {
		  // 读取操作
		  readTodos () {
		    return JSON.parse(localStorage.getItem(TODOS_KEY) || '[]')
		  },
		  // 写入操作
		  saveTodos (todos) {
		    localStorage.setItem(TODOS_KEY, JSON.stringify(todos))
		  }
		}

##localStorage就相等于一个cookie

1. 先设置cookie值
2. 再获取cookie值
	
	// 验证浏览器时是否支持localStorage
	if(window.localStorage){
	   //localStorage是一个对象
	   localStorage.setItem('t2',"李四")
	
	}else{
	    alert('不支持')
	}
	
	console.log(localStorage.getItem('t2'))
	
	</script>

##H5 localStorage 删除操作

1. localStorage.removeItem() //清除一条记录
2. localStorage.clear() 清除所有记录
3. localStorage.length  获取多少键
4. localStorage.key() 获取存储的键内容

##localStorage就相等于模拟的一个数据库

1. localStorage.lenght 查看localStorage中存储有多少条记录
2. localStorage.key()  输出指定的记录内容
3. localStorage.getItem(localStorage.key(0)) 输出第一条记录的内容
4. 长久存储 
5. localStorage.t1="0000"  向数据库中存储一条信息 字段为t1 字段值
6. localStorage.t2="1111"  向数据库中存储一条循序 字段为t2 字段值
7. localStorage.getItem('t3','222') 向数据库中存储一条信息 字段为t3 字段值


##读取数据库中的信息

1. localStorage.t1
2. localStorage['t3']
3. localStorage.getItem('t2')


		<script>
		
			localStorage.t1="000"
			
			localStorage['t2']="111"
			
			localStorage.setItem('t3','222')
			
			for(let i=0;i<localStorage.length;i++){
			  
			  document.write(localStorage.getItem(localStorage.key(i))+'</br>')
			
			}
		
		
		</script>