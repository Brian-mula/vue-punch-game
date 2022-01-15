<template>
    <div>
        <!-- bag -->
        <div id="bag" v-bind:class="{burst:ended}"></div>

        <!-- bag health -->
        <div id="bag-health">
            <div v-bind:style="{width:health + '%'}"></div>
        </div>

        <!-- controlls -->
        <div id="controlls">
            <button v-show="!ended" @click="punch">Punch</button>
            <button @click="restart">Restart</button>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            health:100,
            ended:false
            
        }
    },
    methods:{
        punch(){
            this.health -=10;
            if(this.health <=0){
                this.ended=true
            }
        },
        restart(){
            this.health=100
            this.ended=false
        }

    }
}
</script>
<style scoped>
#bag{
    width:200px;
    height: 500px;
    margin: 0 auto;
    background: url(/img/bag.png) center no-repeat;
    background-size: 80%;
}
#bag.burst{
    background: url(/img/bag-burst.png) center no-repeat;
    background-size: 80%;
}
#bag-health{
    width: 200px;
    border: 2px solid #000;
    margin: 0 auto 20px auto;
}
#bag-health div{
    height: 20px;
    background: crimson;

}
#controlls{
margin: 0 auto;
width: 120px;
}
</style>