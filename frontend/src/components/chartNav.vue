<template>
    <nav class="text-[.9rem]">
        <ul class="flex justify-between items-center">
            <li v-for="item in items" :key="item.path " >
                <button class="hover:bg-slate-200 hover:text-black text-slate-200 px-[1.2em] py-[.6em] rounded"  @click="navigateTo(item.path)" :id="item.chemicalId" :class="{active : isActive(item.path)}">{{ item.chemicalName }}</button>

            </li>
        </ul>
    </nav>
</template>

<script>

    export default{
        data(){
            return{
                items:[
                    {chemicalName: "Carbon Dioxide", chemicalId:"carbon", path:'/'},
                    {chemicalName: "Humidity", chemicalId:"humi", path:'/hum'},
                    {chemicalName: "Pressure", chemicalId:"pressure", path:'/pressure'},
                    {chemicalName: "Temperature", chemicalId:"temp", path:'/temp'},
                    {chemicalName: "LPG", chemicalId:"lpg", path:'/lpg'},
                ],
                currentPath: '/'
            }
        },
        methods: {
            navigateTo(path){
                this.currentPath = path
            },
            isActive(path){
                return this.currentPath === path
            }
        }
    }

</script>
