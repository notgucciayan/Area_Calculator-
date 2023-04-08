# Area_Calculator-
Calculates ares for geometry shapes
<!DOCTYPE html>
<html lang="en">
<head>
    <style>
        .Darkmode2{
            color:white;
            background:black;
        }
        .Darkmode{
            color:white;
            background:black;
        }
     .div1{
         
         padding:20px 20px 20px 20px;
         text-align: center;
         color: Black;
         border:outset 3px;
         background: white;
     }   
     body{
        
     }
     .div2{
         color : black;
         background: white;
         backdrop-filter: blur(100px);
         text-align: center;
         padding-bottom: 20px;
         border: inset 1px;
         
     }
     .button4{
         margin: 0% 0% 0% 43%;
         color:white;
     }
     .div2 input[type="button"]{
     border:outset 5px white;
         background: ;
         color:black;
     }
     .div2 input[type="number"]{
         border: inset grey;
     }
     
.     
    </style>
    <meta charset="UTF-8">
    <title>Page title</title>
</head>
<body>
  <div class="div1">
      <div style="border:outset;"><h1><tt>Area Calculator</tt></h1></div>
    
  </div>  
  <div class="div2">
   <input type="button" value="Rectangle" class="rect"> <br>
   <input type="button" value="Square" class="square"> <br>
   <input type="button" value="Circle" class="circle"> <br>
   <select class="op">
       <option>More</option>
       <option>Rhombus</option>
       <option>parallelogram</option>
   </select>
     
 <strong>   <i style="font-family: monoscope;">
     <form>
        <p class="p1"></p><input type="number" id="p1t">
        <p class="p2"></p><input type="number" id="p2t"><br>
         <input type="reset" style="margin: 3% 0% 0% 1%;color:white;background: maroon;" value="clear">
         
    </i>     </strong>
    <h3 class="h1"></h3>
    <h6 id="F"></h6>
    </form>
  </div>
  
  <button type="submit"style="background: black;" class="button4">Get Area</button>

 
</body>
<script>
    let p1 = document.querySelector(".p1");
    let p2 = document.querySelector(".p2");
    let p1t, p2t, p3t;
    let check = document.querySelector(".rect");
    let check1 = document.querySelector(".circle");
    let check2 = document.querySelector(".square");
    let but = document.querySelector("button");
        p1t = document.querySelector("#p1t");
        p2t = document.querySelector("#p2t");
        let check3 = document.querySelector(".op");
       
  
    var area;
    
    check.addEventListener("click", function() {    
        p1.innerText = "enter length:";
        p2.innerText = "enter breadth:";     
        let input2 = document.querySelector("#p2t")
        input2.style.border ="inset";
        
    });

    check1.addEventListener("click", function() {    
        p1.innerText = "enter radius:";
        p2.innerText = "";       
        let input2 = document.querySelector("#p2t")
        input2.style.border ="none";
        
    });

    check2.addEventListener("click", function() {    
        p1.innerText = "enter side:";     
        p2.innerText = "";
        let input2 = document.querySelector("#p2t")
        input2.style.border ="none";
    });
    
    check3.onchange=function () {
        if (check3.value == "Rhombus") {
             p1.innerText = "enter length :";
             p2.innerText = "enter breadth:";     
        let input2 = document.querySelector("#p2t")
        input2.style.border ="inset";
        
        }
        
        if (check3.value=="parallelogram") {
             p1.innerText = "enter base:";
             p2.innerText = "enter perpendicular height:";     
        let input2 = document.querySelector("#p2t")
        input2.style.border ="inset";
        }
    }

    but.addEventListener("click", function() {
       
        
        if (p1.innerText ==="enter length:") {
            area = p1t.value * p2t.value;
            document.querySelector(".h1").innerText ="Area of Rectangle = " + area;
            console.log(area);
           document.querySelector("#F").innerText = "Formulla:length × breadth"
           
        }
        
         else if (p1.innerText ==="enter radius:") {
            area = 22/7 * p1t.value**2;
            document.querySelector(".h1").innerText ="Area of Circle = " + area;
            console.log(area);
            document.querySelector("#F").innerText ="Formulla:πr²"
            
        } 
        
        else if (p1.innerText ==="enter side:") {
            area = p1t.value **2;
            document.querySelector(".h1").innerText ="Area of Square = " + area;
            console.log(area);
            document.querySelector("#F").innerText ="Formulla:side²"
          
          
        }
        
        else if (p1.innerText ==="enter length :") {
            area = p1t.value*p2t.value /2;
            document.querySelector(".h1").innerText ="Area of Rhombus = " + area;
            console.log(area);
            document.querySelector("#F").innerText ="Formulla:length×breadth÷2"
          
          
        }
        
        else if (p1.innerText ==="enter base:") {
            area = p1t.value*p2t.value;
            document.querySelector(".h1").innerText ="Area of parallelogram = " + area;
            console.log(area);
            document.querySelector("#F").innerText ="Formulla:base × perpendicular height"
          
          
        }
                
                
            });
         
       
    
 </script>
 </html>
