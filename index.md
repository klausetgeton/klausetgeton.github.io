<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>

<button id="test-me">Open tab</button>



<script>
	var testMe = document.getElementById('test-me');

	testMe.addEventListener('click', function() {
		var windowTest = window.open('https://google.com');

		if (!windowTest) {
			alert('It failed to request for new window tab');
			return;
		}
	
		alert('It worked!, closing the tab on 2s...');
		
		setTimeout(function() {
			windowTest.close();
		}, 2000);
	} );
</script>
</body>
</html>
