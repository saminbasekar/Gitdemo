#Demo Git repository 
This is the first file in this repo.

##Ipsum Below##

The Songs of Ascent are a special group of psalms comprising Psalms 120—134. They are also called Pilgrim Songs. Four of these songs are attributed to King David (122, 124, 131, 133) and one to Solomon (127), while the remaining ten are anonymous.

The city of Jerusalem is situated on a high hill. Jews traveling to Jerusalem for one of the three main annual Jewish festivals traditionally sang these songs on the “ascent” or the uphill road to the city. According to some traditions, the Jewish priests also sang some of these Songs of Ascent as they walked up the steps to the temple in Jerusalem.

Each of the psalms in this collection begins with the title “A Song of Ascents.” While perhaps they were not originally composed for this purpose, these psalms were later grouped together for use in traveling toward Jerusalem for the yearly Jewish festivals.

The theme of each Song of Ascent offers much encouragement for those who seek to worship God today:

<!DOCTYPE html>
<html>

<head>
	<script src=
"https://cdnjs.cloudflare.com/ajax/libs/mathjs/10.6.4/math.js"
		integrity=
"sha512-BbVEDjbqdN3Eow8+empLMrJlxXRj5nEitiCAK5A1pUr66+jLVejo3PmjIaucRnjlB0P9R3rBUs3g5jXc8ti+fQ=="
		crossorigin="anonymous"
		referrerpolicy="no-referrer"></script>
	<script src=
"https://cdnjs.cloudflare.com/ajax/libs/mathjs/10.6.4/math.min.js"
		integrity=
"sha512-iphNRh6dPbeuPGIrQbCdbBF/qcqadKWLa35YPVfMZMHBSI6PLJh1om2xCTWhpVpmUyb4IvVS9iYnnYMkleVXLA=="
		crossorigin="anonymous"
		referrerpolicy="no-referrer"></script>
	<!-- for styling -->
	<style>
		table {
			border: 1px solid black;
			margin-left: auto;
			margin-right: auto;
		}

		input[type="button"] {
			width: 100%;
			padding: 20px 40px;
			background-color: green;
			color: white;
			font-size: 24px;
			font-weight: bold;
			border: none;
			border-radius: 5px;
		}

		input[type="text"] {
			padding: 20px 30px;
			font-size: 24px;
			font-weight: bold;
			border: none;
			border-radius: 5px;
			border: 2px solid black;
		}
	</style>
</head>
<!-- create table -->

<body>
	<table id="calcu">
		<tr>
			<td colspan="3"><input type="text" id="result"></td>
			<!-- clr() function will call clr to clear all value -->
			<td><input type="button" value="c" onclick="clr()" /> </td>
		</tr>
		<tr>
			<!-- create button and assign value to each button -->
			<!-- dis("1") will call function dis to display value -->
			<td><input type="button" value="1" onclick="dis('1')"
						onkeydown="myFunction(event)"> </td>
			<td><input type="button" value="2" onclick="dis('2')"
						onkeydown="myFunction(event)"> </td>
			<td><input type="button" value="3" onclick="dis('3')"
						onkeydown="myFunction(event)"> </td>
			<td><input type="button" value="/" onclick="dis('/')"
						onkeydown="myFunction(event)"> </td>
		</tr>
		<tr>
			<td><input type="button" value="4" onclick="dis('4')"
						onkeydown="myFunction(event)"> </td>
			<td><input type="button" value="5" onclick="dis('5')"
						onkeydown="myFunction(event)"> </td>
			<td><input type="button" value="6" onclick="dis('6')"
						onkeydown="myFunction(event)"> </td>
			<td><input type="button" value="*" onclick="dis('*')"
						onkeydown="myFunction(event)"> </td>
		</tr>
		<tr>
			<td><input type="button" value="7" onclick="dis('7')"
						onkeydown="myFunction(event)"> </td>
			<td><input type="button" value="8" onclick="dis('8')"
						onkeydown="myFunction(event)"> </td>
			<td><input type="button" value="9" onclick="dis('9')"
						onkeydown="myFunction(event)"> </td>
			<td><input type="button" value="-" onclick="dis('-')"
						onkeydown="myFunction(event)"> </td>
		</tr>
		<tr>
			<td><input type="button" value="0" onclick="dis('0')"
						onkeydown="myFunction(event)"> </td>
			<td><input type="button" value="." onclick="dis('.')"
						onkeydown="myFunction(event)"> </td>
			<!-- solve function call function solve to evaluate value -->
			<td><input type="button" value="=" onclick="solve()"> </td>

			<td><input type="button" value="+" onclick="dis('+')"
						onkeydown="myFunction(event)"> </td>
		</tr>
	</table>

	<script>
		// Function that display value
		function dis(val) {
			document.getElementById("result").value += val
		}

		function myFunction(event) {
			if (event.key == '0' || event.key == '1'
				|| event.key == '2' || event.key == '3'
				|| event.key == '4' || event.key == '5'
				|| event.key == '6' || event.key == '7'
				|| event.key == '8' || event.key == '9'
				|| event.key == '+' || event.key == '-'
				|| event.key == '*' || event.key == '/')
				document.getElementById("result").value += event.key;
		}

		var cal = document.getElementById("calcu");
		cal.onkeyup = function (event) {
			if (event.keyCode === 13) {
				console.log("Enter");
				let x = document.getElementById("result").value
				console.log(x);
				solve();
			}
		}

		// Function that evaluates the digit and return result
		function solve() {
			let x = document.getElementById("result").value
			let y = math.evaluate(x)
			document.getElementById("result").value = y
		}

		// Function that clear the display
		function clr() {
			document.getElementById("result").value = ""
		}
	</script>
</body>

</html>
