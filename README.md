# OCTANET_JUNE
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width,initial">
        <title> TO DO List </title>
        <style>
            body {
                margin:0;
                background-color:aqua;
            }
            h1 {
                color:rgb(122, 122, 236);
                text-align: center;
            }
            div{
                margin: 20px;
                padding: 10px;
                background-color: brown;
                box-shadow: 3px 5px 6px rgb(0, 1, 0);
                border-radius: 25px;
            }
            #container {
                margin:25;
                padding:25;
                color:rgb(47, 3, 89);
                background-color: rgb(226, 128, 42);
                text-align: center;
            }
            #input {
                color:rgb(239, 86, 15);
                background-color: rgb(53, 53, 167);
                border: 2px;
                border-bottom: 2px solid #da5f5f;
                border-left: 2px solid #876bef;
            }
            #btn {
                border: 1px;
                border-radius: 10px;
                background-color: rgb(232, 70, 157);
            }
        </style>
        </head>
        <body>
            <div>
                <h1> TO DO List </h1>
            </div>
            <div id="container">
                <input type="text" id="input" placeholder="enter your text">
                &nbsp;&nbsp;&nbsp;
                <button id="btn"> ADD New TODO</button>
                <ul class="ul" style="list-style-type:none;">
                </ul>
            </div>
        </body>
        <script>
            document.getElementById('btn').addEventListener('click',
            function() {
                let input = document.getElementById('input').value;


                //creating a to do list
                let elem= document.createElement('li');
                let btn1= document.createElement('button');
                let btn2= document.createElement('button');
                btn1.innerText= "Complete";
                btn2.innerText= "Remove";
                elem.innerText= "Task Input";
                let ul=document.querySelector('ul');

                //appending the created elements to html
                ul.appendChild(elem);
                elem.appendChild(btn1);
                elem.appendChild(btn2);
                //adding style to list
                btn1.style.border="none";
                btn1.style.marginLeft="3%";
                btn1.style.borderRadius="8px";
                btn1.style.backgroundColor="#b4b3d8"
                btn2.style.border="none";
                btn2.style.marginLeft="3%";
                btn2.style.borderRadius="8px";
                btn2.style.backgroundColor="#b4b3d8"
                //addind functionality to created buttons
                btn1.addEventListener('click',
                    function(){
                        elem.style.textDecoration="line-through"; 
                    }
                );
                btn2.addEventListener('click',
                    function(){
                        elem.remove(); 
                    }
                );

                document.getE1elementbyId('input').value="";
            }
            );
             </script>
             </html>
