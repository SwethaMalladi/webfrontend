<template>
<div>
    <h2><b> {{headername}}</b></h2>
    </div>
    <!--<h2><b> {{UniversityName}}</b></h2> -->
</template>
<script>
export default{
    name: 'MyHeader',
    props:{
        headername: String,
        //UniversityName:String //
    }
}
</script>
<style scoped>
div{
    text-align: center;
    padding: 0% 20%;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    color: rgb(255, 0, 221);
    font-size: 2rem;
    font-weight: bold;
    text-transform: uppercase;
}
</style>