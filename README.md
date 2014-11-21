<!doctype html>
<html>
<head>
<meta charset="UTF-8">
<title>Examen</title>
		<!--Jquery--->
		<script src="http://code.jquery.com/jquery-latest.min.js"></script>
		<script src="http://code.jquery.com/color/jquery.color-2.1.2.js"></script>
		
		<style type="text/css">
			.clear{
				clear:both;
			}
			
			body{
				background-color:#F93;
			}
			
			h1 {
				font-family: Helvetica, sans-serif;
				font-size:50px;
				color:#FFF;
				margin:10px 10px;
			}
			
			#contenderDias{
				width:350px;
				margin-right:auto;
				
			}
				
			#contenderMeses{
				width:350px;
				margin-right:auto;
				
			}
			
			.cuadrosDias {
				width: 50px;
				height: 50px;
				float: left;
				margin:10px 10px;
				/*background: #de9301;*/
				background:#FFC;
			}
			
			.cuadrosMeses {
				width: 20px;
				height:20px;
				float: left;
				margin:10px 10px;
				/*background: #01c7de;*/
				background:#FFC;
			}
			
		</style>
		
		
	</head>

	<body>
		
		<h1>DÍAS:</h1>
		<div id="contenderDias"></div>
		<div class="clear"></div>
		<h1>MESES:</h1>
		<div id="contenderMeses"></div>
	
		<script type="text/javascript" charset="utf-8">
		
   		var fecha = new Date();
		var dias = fecha.getDate()//Return the day of the month
		var meses = fecha.getMonth()//The getMonth() method returns the month (from 0 to 11) for the specified date, according to local time. Note: January is 0, February is 1, and so on.


	
			
			
			//alert(dias);
			//alert(meses);
			
			function crearDias(){
		
				for(i= 1; i<=dias; i++){
					$('#contenderDias').append('<div class="cuadrosDias"></div>')
				};//The append() method inserts specified content at the end of the selected elements.
			};
			
			function crearMeses(){
					
				for(i= 0; i<=meses; i++){
					$('#contenderMeses').append('<div class="cuadrosMeses"></div>')
				};

			};
			
			crearDias();
			crearMeses();
			
			$(document).ready(function() {
			
			$(".cuadrosDias").click(function(){
				$(this).fadeOut(5000);//Al dar click van a desaparecer
			});
			
			$(".cuadrosMeses").click(function(){
				$(this).fadeOut(5000);
			});
			
		
			})
			
		</script>
	
	</body>
	
</html>
