
<!DOCTYPE html>

<html>

<head>



    <meta name="viewport" content="width=device-width, initial-scale=1">

    <meta charset = "utf-8">

    <link rel="stylesheet" href="http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.css">

    <link rel="stylesheet" href="styles/styles.css">

    <link rel="stylesheet" href="https://ajax.googleapis.com/ajax/libs/jqueryui/1.11.4/themes/smoothness/jquery-ui.css">



    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>

    <script src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.11.4/jquery-ui.min.js"></script>

    <script src="http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.js"></script>

<style>

#options div{

  background:#000000;

  color: #000000;

  display: inline-block !important;

  height: 35px;

  line-height: 50px;

  text-align: center;

  vertical-align: top;

  width: 50px;

}



#slices img{ 

  display: inline-block;

  height: 30px;

}



#area{

 

}

</style>

  <script>

        $( document ).on( "pagecreate", function() {

            $( ".photopopup" ).on({

                popupbeforeposition: function() {

                    var maxHeight = $( window ).height() - 60 + "px";

                    $( ".photopopup img" ).css( "max-height", maxHeight );

                }

            });

        });



        $(document).on("ready", function(){



            var slices = $("#slices");

            var options = $("#options");

            var area = $("#area");



            var selected;

            var result;



            //---Array of images

            var pizzas = [

            {image: "http://s23.postimg.org/6yojml8vb/Pizza_One.png", value: 1},

            {image: "http://s13.postimg.org/5d8zxnb2b/pizzatwo.png", value: 2},

            {image: "http://s12.postimg.org/xfsxldqyx/pizzathree.png", value: 3},

            {image: "http://s14.postimg.org/d6tdq0865/pizzafour.png", value: 4}

            ];

            var total = pizzas.length;



            //---Make boxes dragables

            options.find("div").draggable();



            //---When the boxes are dropped

            area.droppable({



                drop: function(event, ui){



                    console.log("yes");



                    if( Number( ui.draggable.attr("data-index") ) == result ){



                        alert("correct");



                    }else{



                        alert("incorrect");



                    }



                }



            });



            //---Insert random pizza slices

            function insertPizzas(){



                selected = [];

                result = 0;



            //---Generate aleatory pieces

            var rand



            while(selected.length < 2){



            //---Random value

            rand = Math.floor( Math.random() * total );



            //---Sum result

            result += pizzas[rand].value;



            selected.push( rand );



            }



            //---Clear the slices

            slices.html("");



            //---Add the new slices

            selected.forEach(function(number){



                var img = $("<img/>");



                img.attr("src", pizzas[number].image);



                slices.append(img);



            });



            }



            insertPizzas();



        });

    </script>



<SCRIPT LANGUAGE="JavaScript">



var theImages = new Array() 





theImages[1]="http://s23.postimg.org/6yojml8vb/Pizza_One.png"

theImages[2]="http://s13.postimg.org/5d8zxnb2b/pizzatwo.png"

theImages[3]="http://s12.postimg.org/xfsxldqyx/pizzathree.png"

theImages[4]="http://s14.postimg.org/d6tdq0865/pizzafour.png"

theImages[5]="http://s14.postimg.org/t7lz2z61p/pizzafive.png"

theImages[6]="http://s1.postimg.org/69fub6h9n/pizza6.png"

theImages[7]="http://s8.postimg.org/qo6xa8ve9/pizza7.png"

theImages[8]="http://s10.postimg.org/bft4if0z9/wholepie.png"





var j = 0

var p = theImages.length;

var preBuffer = new Array()

for (i = 0; i < p; i++){

   preBuffer[i] = new Image()

   preBuffer[i].src = theImages[i]

}

var whichImage = Math.round(Math.random()*(p-1));

function showImage(){

document.write('<img src="'+theImages[whichImage]+'">');

}



</script>



<SCRIPT LANGUAGE="JavaScript">


var theImagesOne = new Array() 





theImagesOne[1]="http://s23.postimg.org/6yojml8vb/Pizza_One.png"

theImagesOne[2]="http://s13.postimg.org/5d8zxnb2b/pizzatwo.png"

theImagesOne[3]="http://s12.postimg.org/xfsxldqyx/pizzathree.png"

theImagesOne[4]="http://s14.postimg.org/d6tdq0865/pizzafour.png"

theImagesOne[5]="http://s14.postimg.org/t7lz2z61p/pizzafive.png"

theImagesOne[6]="http://s1.postimg.org/69fub6h9n/pizza6.png"

theImagesOne[7]="http://s8.postimg.org/qo6xa8ve9/pizza7.png"

theImagesOne[8]="http://s10.postimg.org/bft4if0z9/wholepie.png"





var a = 0

var b = theImagesOne.length;

var preBufferOne = new Array()

for (z = 0; z < b; z++){

   preBufferOne[z] = new Image()

   preBufferOne[z].src = theImagesOne[z]

}

var whichImageOne = Math.round(Math.random()*(b-1));

function showImageOne(){

document.write('<img src="'+theImagesOne[whichImageOne]+'">');

}



</script>





<style>

        .draggable { width: 75px; height: 150px; padding: 0.5em; float: right;margin: 10px 10px 10px;}

    </style>

<style>

.drop { width: 60px; height: 60px; border: 5px solid gray; position: absolute; top: 270px; left: 600px; }

</style>

<style>

.drop1 { width: 60px; height: 60px; border: 5px solid gray; position: absolute; top: 470px; left: 600px; }

</style>





 



 

  

  <script>

        $(function() {

            $( "#draggable1" ).draggable();

        });

  </script>

 <script>

        $(function() {

            $( "#draggable2" ).draggable();

        });

  </script>

 <script>

        $(function() {

            $( "#draggable3" ).draggable();

        });

  </script>

 <script>

        $(function() {

            $( "#draggable4" ).draggable();

        });

  </script>

 <script>

        $(function() {

            $( "#draggable5" ).draggable();

        });

  </script>

 <script>

        $(function() {

            $( "#draggable6" ).draggable();

        });

  </script>

 <script>

        $(function() {

            $( "#draggable7" ).draggable();

        });

  </script>

 <script>

        $(function() {

            $( "#draggable8" ).draggable();

        });

  </script>

<script>

$( ".drop" ).droppable({

  drop: function( event, ui ) {

    var off = $( this ).offset();

    off.top += 500;

    off.left += 500;

    ui.draggable.offset( off );

  }

});

</script>

<script>

$( ".drop1" ).droppable({

  drop: function( event, ui ) {

    var off = $( this ).offset();

    off.top += 500;

    off.left += 500;

    ui.draggable.offset( off );

  }

});

</script>

<script>

$( document ).on( "pagecreate", function() {

    $( ".photopopup" ).on({

        popupbeforeposition: function() {

            var maxHeight = $( window ).height() - 60 + "px";

            $( ".photopopup img" ).css( "max-height", maxHeight );

        }

    });

});

</script>



<script>$('#widget').draggable();</script>





 <style type="text/css">

body {

    background-image: url("http://s21.postimg.org/9bj52fal3/sdfsdfdsf.jpg");

    background-repeat: no-repeat;

    background-position: right top;

    margin-right: 200px;

    background-attachment: fixed;

    background-size:100% 100%;

}

.ui-page {

    background: transparent;

}

.ui-content{

    background: transparent;

}



</style>



<style type="text/css">

body {

    background-repeat: no-repeat;

    background-position: right top;

    

    background-attachment: fixed;

    background-size:100% 100%;

}

.ui-page {

    background: transparent;

}

.ui-content{

    background: transparent;



}



body.class1 {

    background-image:url('http://s12.postimg.org/rwwd40y4t/Jungle_Background.jpg');

}



body.class2 {

    background-image:url('http://upload.wikimedia.org/wikipedia/commons/e/ec/Pattern_square_16.png');

}



body.class3 {

    background-image:url('http://www.herbactive.com.br/catalog/view/theme/default/image/pattern/pattern-11.png');

}

</style>

<style>

#rotimg {

  transform: rotate(360deg) ;

  animation: rotate linear 3s infinite;

}



@keyframes rotate {

  0% {

    transform: rotate(0);

  }

  100% {

    transform: rotate(360deg);

  }

}

</style>



<script type="text/javascript">

        $(document).ready(function () {

            $('#source li').draggable({

                helper: 'clone',

                revert: 'invalid'

            });



            $('#answerfour').droppable({

                accept: 'li[data-value="four"]',

                drop: function (event, ui) {

                    $('#four').append(ui.draggable);

                }

            });



            $('#four').droppable({

                accept: 'li[data-value="four"]',

                drop: function (event, ui) {

                    $('#cities').append(ui.draggable);

                }

            });

        });

    </script>

    <style>

        .divClass {

            border: 3px solid black;

            font-size: 25px;

            background-color: purple;

            width: 400px;

            padding: 5px;

            display: inline-grid;

        }



        li {

            font-size: 20px;

        }

    </style>



</head>

<body>





<div data-role="page" id="pageone">



 <embed src="http://soundimage.org/wp-content/uploads/2015/09/Some-Far-Away-Place_v001.mp3" autostart="true" loop="false" hidden="true">



<center><img id="rotimg" src="http://i.imgur.com/WRKKFQz.png" alt="cog1"></center>



    <div data-role="popup" id="myPopup" class="photopopup" data-overlay-theme="a" data-corners="false" data-tolerance="30,15">

      <a href="#" data-rel="back" class="ui-btn ui-corner-all ui-shadow ui-btn-a ui-icon-delete ui-btn-icon-notext ui-btn-right">Close</a><img src="http://s22.postimg.org/xqt2gakyp/Math_Howto_Image.png" alt="Photo portrait">



    </div>





 

  <div data-role="main" class="ui-content">





<div data-role="footer" data-id="foo2" data-position="fixed">

  <div data-role="navbar">

    <ul>

      <li><a href="#myPopup" data-rel="popup" data-position-to="window" class="ui-btn ui-btn-b ui-corner-all ui-shadow ui-btn-inline">Game Info!</a></li>

      

      <li><a href="#anylink" data-rel="popup" data-position-to="window" class="ui-btn ui-btn-b ui-corner-all ui-shadow ui-btn-inline">&copy; Arthur Barsuk</a></li>



 <li>

          <a href="#" id="btn1" class="ui-btn ui-btn-b ">Jungle BackGround!</a>



 

  <script>

    $("#btn1").click(function() {

      $('body').removeAttr('class');

      $('body').attr('class', 'class1');

    });



    $("#btn2").click(function() {

      $('body').removeAttr('class');

      $('body').attr('class', 'class2');

    });



    $("#btn3").click(function() {

      $('body').removeAttr('class');

      $('body').attr('class', 'class3');

    });

  </script>

        </li>

         </ul>

  </div>

</div>

   

<div data-role="header" data-id="foo1" data-position="fixed">

    <div data-role="navbar">

        <ul>

            <li><a href="#pagetwo" class="ui-btn ui-btn-b ui-icon-plus "><img src = ' http://s2.postimg.org/d85uobexx/add3232.png'></a></li>

            <li><a href="#pagethree" class="ui-btn ui-btn-b ui-icon-minus "btn-b"> <img src = ' http://s17.postimg.org/6s9gx9i9n/minus3232.png'></a></li>

            <li><a href="#pagefour" class="ui-btn ui-btn-b ui-icon-delete "btn-b" > <img src = 'http://s4.postimg.org/thfw9ljft/3232mult.png'></a></li>

           

        </ul>

    </div><!-- /navbar -->

</div><!-- /footer -->



                

   



</div>

 







</div>

<div data-role="page" id="pagetwo">





<div data-role="popup" id="myPopup2" class="photopopup" data-overlay-theme="a" data-corners="false" data-tolerance="30,15">

      <a href="#" data-rel="back" class="ui-btn ui-corner-all ui-shadow ui-btn-a ui-icon-delete ui-btn-icon-notext ui-btn-right">Close</a><img src="http://s1.postimg.org/ljwm4953z/Screen_Shot_2015_12_12_at_10_45_52_PM.png" alt="Photo portrait">



    </div>





  <div data-role="main" class="ui-content">

       

       <div data-role="header" data-id="foo1" data-position="fixed">

    <div data-role="navbar">

        <ul>

            <li><button onclick="location.reload(true)" class ="ui-btn-b">New Pizzas!</button></li>

            <li><a href="#myPopup2" data-rel="popup" data-position-to="window" class="ui-btn ui-btn-b ui-corner-all ui-shadow ui-btn-inline">How To Play</a></li>

        </ul>

    </div><!-- /navbar -->

</div><!-- /footer -->

<div data-role="footer" data-id="foo1" data-position="fixed">

    <div data-role="navbar">

        <ul>

            <li><a href="#pageone" class="ui-btn ui-btn-b ui-icon-home ui-btn-icon-left">Home</a></li>

        </ul>

    </div><!-- /navbar -->

</div><!-- /footer -->

<center> <font size="5" color="#FACC2E"> <b> Add the Slices!!</b></font></center>
<center><div id="slices"></center>

  

</div>
<br>

<div id="options">

  <div data-index="1"> <img src="http://s28.postimg.org/p4r3cyqe1/Number_One.png;"></div>

  <div data-index="2"> <img src="http://s15.postimg.org/6w8stssxj/NUMBERtwo.png;"></div>

  <div data-index="3"> <img src="http://s3.postimg.org/c5qy5oobz/NUMBERthree.png;"></div>

  <div data-index="4"><img src="http://s2.postimg.org/7wbdmd22t/NUMBERfour.png;"></div>

  <div data-index="5"><img src="http://s29.postimg.org/91zaeovsj/NUMBERfive.png;"></div>

  <div data-index="6"><img src="http://s3.postimg.org/ayhlr7nlb/NUMBERsix.png;"></div>

  <div data-index="7"><img src="http://s27.postimg.org/wl2xy5ksv/NUMBERseven.png;"></div>

  <div data-index="8"><img src="http://s7.postimg.org/4q44dy6h3/NUMBEReight.png;"></div>

</div>

<br>
<center>
<div id="area">

<img src= "http://s21.postimg.org/4f94f8rkn/empty_pizza_box.png;">

</div>

 </center> 























</div>

  







</div>











<div data-role="page" id="pagethree">



<div align="center">



  

        <div class="divClass">

             

 

Subtract the Slices and drag them to the right box!

                <ul id="source">

                    <li data-value="four"><img src = 'http://s22.postimg.org/ldg3b06q9/two_pizza_slices.png'></li>

                    

                </ul>

        </div>



        <div class="divClass" id="answertwo">

             <img src = ' http://s17.postimg.org/axajm2j6z/pizzaboxcolor4.jpg'>

            <ul id="countries"></ul>

        </div>



        <div class="divClass" id="answereight">

             <img src = 'http://s18.postimg.org/6hipfjm45/pizzaboxcolor8.jpg'>

            <ul id="eight"></ul>

        </div>



  <div class="divClass" id="answersix">

             <img src = ' http://s2.postimg.org/xs40tuvxx/pizzaboxcolor6.jpg'>

            <ul id="countries"></ul>

        </div>



  <div class="divClass" id="answerfour">

         <img src = ' http://s7.postimg.org/9vuqfmygn/pizzaboxcolor0.jpg'>

            <ul id="four"></ul>

        </div>

        </div>

<div data-role="popup" id="myPopup3" class="photopopup" data-overlay-theme="a" data-corners="false" data-tolerance="30,15">

      <a href="#" data-rel="back" class="ui-btn ui-corner-all ui-shadow ui-btn-a ui-icon-delete ui-btn-icon-notext ui-btn-right">Close</a><img src="http://s17.postimg.org/4z4wjjg33/subtract.png" alt="Photo portrait">



</div>

 

  <div data-role="main" class="ui-content">

    <div data-role="header" data-id="foo1" data-position="fixed">

    <div data-role="navbar">

        <ul>

            <li><button onclick="location.reload(true)" class ="ui-btn-b">New Pizzas!</button></li></li>

            <li><a href="#myPopup3" data-rel="popup" data-position-to="window" class="ui-btn ui-btn-b ui-corner-all ui-shadow ui-btn-inline">Game Info!</a></li>

            

        </ul>

    </div><!-- /navbar -->

</div><!-- /footer -->



    <div data-role="footer" data-id="foo1" data-position="fixed">

    <div data-role="navbar">

        <ul>

            <li><a href="#pageone" class="ui-btn ui-btn-b ui-icon-home ui-btn-icon-left">Home</a></li>

        </ul>

    </div><!-- /navbar -->

</div><!-- /footer -->



 











</div>

</div>



<div data-role="page" id="pagefour">

<div align="center">

  



       <div class="divClass"> 

            Your Cake Image! <br>

How many Candles do we have? <br>

Drag the cakes to your answer!

                <ul id="source">

                    <li data-value="four"><img src = ' http://s2.postimg.org/dpqo08e9l/cake2.png'></li>

                    

                </ul>

      

        </div>



        <div class="divClass" id="answertwo">

            2

            <ul id="countries"></ul>

        </div>



        <div class="divClass" id="answerfour">

            4

            <ul id="four"></ul>

        </div>



  <div class="divClass" id="answersix">

            6

            <ul id="countries"></ul>

        </div>



  <div class="divClass" id="answereight">

           8

            <ul id="countries"></ul>

        </div>

</div>

<div data-role="popup" id="myPopup4" class="photopopup" data-overlay-theme="a" data-corners="false" data-tolerance="30,15">

      <a href="#" data-rel="back" class="ui-btn ui-corner-all ui-shadow ui-btn-a ui-icon-delete ui-btn-icon-notext ui-btn-right">Close</a><img src="http://s23.postimg.org/rlde0icjv/multiply.png" alt="Photo portrait">



    </div>





  <div data-role="main" class="ui-content">

       

       <div data-role="header" data-id="foo1" data-position="fixed">

    <div data-role="navbar">

        <ul>

            <li><button onclick="location.reload(true)" class ="ui-btn-b">New Cakes</button></li>

            <li><a href="#myPopup4" data-rel="popup" data-position-to="window" class="ui-btn ui-btn-b ui-corner-all ui-shadow ui-btn-inline">How To Play</a></li>

        </ul>

    </div><!-- /navbar -->

</div><!-- /footer -->

<div data-role="footer" data-id="foo1" data-position="fixed">

    <div data-role="navbar">

        <ul>

            <li><a href="#pageone" class="ui-btn ui-btn-b ui-icon-home ui-btn-icon-left">Home</a></li>

        </ul>

    </div><!-- /navbar -->

</div><!-- /footer -->





</div>



</div>



<div data-role="page" id="pagefive">





<div data-role="popup" id="myPopup5" class="photopopup" data-overlay-theme="a" data-corners="false" data-tolerance="30,15">

      <a href="#" data-rel="back" class="ui-btn ui-corner-all ui-shadow ui-btn-a ui-icon-delete ui-btn-icon-notext ui-btn-right">Close</a><img src="http://s2.postimg.org/bl90jutrt/division.png" alt="Photo portrait">



    </div>





  <div data-role="main" class="ui-content">

       

       <div data-role="header" data-id="foo1" data-position="fixed">

    <div data-role="navbar">

        <ul>

            <li><button onclick="location.reload(true)" class ="ui-btn-b">New Cakes</button></li>

            <li><a href="#myPopup5" data-rel="popup" data-position-to="window" class="ui-btn ui-btn-b ui-corner-all ui-shadow ui-btn-inline">How To Play</a></li>

        </ul>

    </div><!-- /navbar -->

</div><!-- /footer -->

<div data-role="footer" data-id="foo1" data-position="fixed">

    <div data-role="navbar">

        <ul>

            <li><a href="#pageone" class="ui-btn ui-btn-b ui-icon-home ui-btn-icon-left">Home</a></li>

        </ul>

    </div><!-- /navbar -->

</div><!-- /footer -->





</div>





</div>









</body>

</html>
