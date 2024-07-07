# javascript-baasic
## home.html
```
<!DOCTYPE html>
<html>
<head>
    <title>TO DO LIST</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<script>
    const tasks=[];
    function add(){
        title=document.getElementById("t1").value;
        des=document.getElementById("t2").value;
        dat=document.getElementById("t3").value;
        tasks.push({Title:title,Descrip:des,date:dat,complete:false});
        let text = "<ul>";
        tasks.forEach(myFunction);
        text += "</ul>";
    
        // document.getElementById("demo").innerHTML = text;
        function myFunction(value) {
            text += "<li>" + value.Title +" "+value.Descrip+" "+value.date+ "<input type=\"checkbox\">"+"</li>";
        } 
        document.getElementById("demo").innerHTML = text;
    }
    function del(){
        title=document.getElementById("t1").value;
        let i=0;
        let n;
        tasks.forEach(search);
        function search(value){
            if(value.Title==title){
                n=i;
            }
            i+=1;
        }
        tasks.splice(n,n);
        
        let text = "<ul>";
        tasks.forEach(myFunction);
        text += "</ul>";
        function myFunction(value) {
            text += "<li>" + value.Title +" "+value.Descrip+" "+value.date+ "<input type=\"checkbox\">"+"</li>";
        } 
        document.getElementById("demo").innerHTML = text;
    }
    function edit(){
        title=document.getElementById("t1").value;
        des=document.getElementById("t2").value;
        dat=document.getElementById("t3").value;
        let i=0;
        let n;
        tasks.forEach(search);
        function search(value){
            if(value.Title==title){
                n=i;
            }
            i+=1;
        }
        if(des!=""){
            tasks[n].Descrip=des;
        }
        if(dat!=""){
            tasks[n].date=dat;
        }
        
        let text = "<ul>";
        tasks.forEach(myFunction);
        text += "</ul>";
    
        // document.getElementById("demo").innerHTML = text;
        function myFunction(value) {
            text += "<li>" + value.Title +" "+value.Descrip+" "+value.date+ "<input type=\"checkbox\">"+"</li>";
        } 
        document.getElementById("demo").innerHTML = text;
    }
    
</script>

<div class="main">
    <h2>TO DO LIST</h2>
    <p id="demo">No Task</p>
    <div>Title: <input class="srch" id="t1" type="search" name="" placeholder="Enter Title"></div>
    <div>Description: <input class="srch" id="t2" type="text" name="" placeholder="Enter Description"></div>
    <div>Date: <input class="srch" id="t3" type="date" name="" placeholder="Search"></div>
    <button type="button" onclick=add()>ADD</button>
    <button type="button" onclick=edit()>Edit</button>
    <button type="button" onclick=del()>Delete</button>
</div>
</body>
</html>

```

## style.css
```
body {
    font-family: sans-serif;
    background-color: #00a8ff;
  }
.main{
    display:block;
    justify-content: center;
    text-align: center;
    height: 200px;
    width: 100;
}
h2{
    font-size: xx-large;
    padding-bottom: 50px;
}
.main > div{
    padding: 10px;
    font-size:x-large;
}
.main>div>input{
    height:30px;
    width: 200px;
}
.main>button{
    height:30px;
    width: 70px;
}
.main>p{
    padding-bottom: 150px;
    font-size: large;
}
```
## OUTPUT:
![image](https://github.com/Hariharan-061102/javascript-baasic/assets/93427270/2688178d-34af-4e89-aa38-0ab85c802c9e)
