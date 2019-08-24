
##html5 localStorage操作

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
