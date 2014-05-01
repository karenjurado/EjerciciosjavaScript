EjerciciosjavaScript
====================

ejercicios realizados con  html5 y javaScrip

ejercicio que realiza la suma de dos numeros binarios
=======================================================


<script type="text/javascript">
		function calculate() {
			var x = document.getElementById("binary1").value;
			var y = document.getElementById("binary2").value;
		if ((/[^0-1]/g.test(x)) || x == "") {
			document.getElementById("error1").innerHTML="Introduzca un valor binario valido!";
			document.getElementById("binary1").value = "";
		return 0;
		}
			else if ((/[^0-1]/g.test(y)) || y == "") {
			document.getElementById("error2").innerHTML="Introduzca un valor binario valido!";
			document.getElementById("binary2").value = "";
			return 0;
		}
			else
		{
				document.getElementById("error1").innerHTML="";
				document.getElementById("error2").innerHTML="";
			var outputValue=0;
			for(i = x.length-1; i >= 0; i -= 1) {
					outputValue += eval(x.charAt(i)) * Math.pow(2, x.length-i-1);
				}
		var b1 = parseInt(outputValue);
		outputValue=0;
		for(i = y.length-1; i >= 0; i -= 1) {
			outputValue += eval(y.charAt(i)) * Math.pow(2, y.length-i-1);
		}
		var b2 = parseInt(outputValue);
		var res=b1+b2;
		document.getElementById("result1").value= res.toString(2);
		document.getElementById("result2").value= res;
	}
}
</script>
<table><tr><td width="100%">
	<div id="input">
		<table style="margin:0px; width:100%">
			<tr><td  align="center" value="top" id="title"><h2> Suma Binaria</h2></td></tr>
			<tr><td value="top" width="160"><h3 id="input-type">Ingresa el numero binario (A)</h3></td><td><input type="text" id="binary1"> <label id="unit"></label><br /> <label id="error1" class="error"></label ></td></tr>
			<tr><td value="top" width="160"><h3 id="input-type">Ingresa el numero binario (B)</h3></td><td><input type="text" id="binary2"> <label id="unit"></label><br /> <label id="error2" class="error"></label ></td></tr>
			<tr><td align="center"></td><td><input type="button" value="Calcular" id="button" onClick="calculate()"></td><td></td></tr>
		</table>
	</div>
	</td></tr><tr><td style="padding-left:40px;" align="center">
		<div style="width:100%">
		<div style="float:left; width:80px">

		<div class="g-plusone" data-size="medium" ></div>

<script type="text/javascript">
  (function() {
    var po = document.createElement('script'); po.type = 'text/javascript'; po.async = true;
    po.src = 'https://apis.google.com/js/plusone.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(po, s);
  })();
</script>
		</div>
		<div style="float:left;">
		<div id="fb-root"></div>
		<script>(function(d, s, id)
		{
		  var js, fjs = d.getElementsByTagName(s)[0];
		  if (d.getElementById(id)) return;
		  js = d.createElement(s); js.id = id;
		  js.src = "//connect.facebook.net/en_US/all.js#xfbml=1";
		  fjs.parentNode.insertBefore(js, fjs);
		}
			(document, 'script', 'facebook-jssdk'));</script>

</div>
</div>
</td></tr><tr><td>
	<div id="res_area" style="visibility:visible">
		<table>
			<tr><td colspan="2"><font id="res">El resultado es </font></td></tr>
			<tr><td width="120"><label id="conversion-result">A+B en Binario</label>
			</td><td><input type="text" disabled="disabled" class="result" id="result1" /> 
			<label id="unit"></label></td></tr>
			</table>
	 </div>
	 </td></tr>
	 </table>	</div>
			<script type="text/javascript">
			for(i=1;i<=20;i++){
				try{
					var re=document.getElementById("result"+i);
					re.disabled=false;
				}
				catch(e){
					break;
				}
			}
		</script>

