<template>
<div>
	<li v-for='(i,index) in arr' @click='a(index)'>
        {{i.name}}
        <ul   v-if='b==index'>
            <li v-for='con in i.data' >{{con}}</li>
        </ul>
    </li>
</div>
</template>
<script>
    export default{
        data(){
            return{
                b:-1,
                arr:[{'name':'index','data':{'name':'index1',name:'index2'}}
                ,{'name':'CON','data':{'name':'CON1',name:'CON2'}},]
            }
        },
        methods:{
            a(e){
                this.b=e;
            }
        },
		props:{   
			XIA:String
		}
    }
</script>