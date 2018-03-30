<template>
<div>
	账号：<input type='text' id='sss'><br/>
	密码：<input type='text' id='pass'><br/>
	<button @click='aaa(arr)'>提交</button>	

</div>
</template>
<script>
	export default{

		data(){
			return{
				arr:[]
			}
		},
		methods:{
			aaa(arr){
				for(var i=0;i<arr.length;i++){
					if(sss.value==arr[i].name && pass.value==arr[i].pass){
						
						return	console.log('登陆成功');
					}else{
						console.log('登陆失败')
					}
				}
			}
		},
		created(){
			this.$http.get('http://localhost:8000').then((el)=>{
				this.arr = el.body
			})
		}
	}

</script>