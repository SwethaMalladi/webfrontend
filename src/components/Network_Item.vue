<template>
    <div >
        <ul><h4>Name of network {{networks.Name}}</h4></ul>
        <ul><h4>Founder - {{networks.Founder}}</h4></ul>   
        <ul><h4>Plan name - {{networks.Plan_name}}</h4></ul>
        <ul><h4>Prize of plan - ${{networks.Prize}}</h4></ul>
        <ul><h4>Number of subscribers - {{networks.Subscribers}}million</h4></ul>
            <ul><h4>Annual Turn over - ${{networks.Turnover}}Billion</h4></ul>
    </div>
</template>
<script>

export default{
    name: 'Network_Item',
    props:{
        networks: Array,
    }   
    /*methods: {
        getDate(datetime) {
            let date = new Date(datetime);
            let dateString = `${date.getFullYear()}-${date.getDate()}-${date.getMonth() + 1}`
            return dateString
        }
    }*/
}

</script>
<style scoped>

template{
    margin-left: 10%;
    margin-right: 10%;
    margin-top: 10%;
    margin-bottom: 10%;
}


p{
    margin: 2px;
    float: center;
}

.data{
    margin-bottom: 0px;
    bottom: 0;
    float: right;
}

h4{
    margin: 2px;
}

h3{
    margin: 2px;
    float: right;
    bottom: 0px;
}


div{
    width: 50%;
    height: 90%;
    color: rgb(209, 129, 211);
    padding: 1em;
    border-radius: 5px;
    border: 0.3em solid  rgb(235, 244, 240);
    margin-bottom: 25px auto;
    overflow: auto;
    
  }
div:hover {
 border: 0.3em solid rgb(46, 165, 74);
 color: rgb(88, 64, 197);
}


.green{
background-color: rgb(55, 175, 109) !important;

}
.blue{
    
background-color: rgb(133, 100, 195) ;
}
.eventbg{
    width: 1%;
    float: right ;
    position: inherit; top: 0px;
}

</style>