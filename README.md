<!DOCTYPE html>
<html lang="en">
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>HTML</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@100;400&display=swap" rel="stylesheet">
<style>	
	.column {
	  float: left;
	  width: 30%;
	  padding: 5px;
	}
	img {
	  width: 100%;
	}	

	.container {
    display:flex;
    background:rgb(216, 217, 222);
    height:25vw;
}
.content {
    position:relative;
    flex:1;
    width:100%;
    height:calc(100% - 2em);
    margin:.5em .5em 1.5em;
    background:white;
}
.content:hover {
    background:rgb(106, 149, 192);
}
.content:hover:after {
    content:attr(data-legend);
    position:absolute;
    left:0;
    bottom:0;
    right:0;
    text-align:center;
	font-family: 'Roboto', sans-serif;
    transform:translateY(100%);
}

body h2 {
	font-family: 'Roboto', sans-serif;
}

</style>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
	<script>
		$('DIV#images img').click(function () {
    		$('DIV #text').html($(this).data('text'));
		});
	</script>
</head>  
<body>
    <h2>Review of Transformation URL API</h2>

	<div class="container">
		<div class="content" data-legend="Original Image"><a href="https://res.cloudinary.com/demo/image/upload/bike.jpg" target="_blank"><img src="https://res.cloudinary.com/demo/image/upload/bike.jpg" alt="image1" data-text="this is one"></a></div>
		<div class="content" data-legend="Q Auto"><img src="https://res.cloudinary.com/chriszak/image/fetch/q_auto/http://res.cloudinary.com/demo/image/upload/bike.jpg" alt="image1" data-text="this is two"></div>
		<div class="content" data-legend="Q Auto - F Auto - Lossy"><img src="http://res.cloudinary.com/chriszak/image/fetch/q_auto,f_auto,fl_lossy/http://res.cloudinary.com/demo/image/upload/bike.jpg" alt="image1" data-text="this is three"></div>
	</div>
	<div style="height: 100px;"></div>
	<div class="container">
		<div class="content" data-legend="last image"><img src="https://res.cloudinary.com/chriszak/image/fetch/q_auto,f_auto,fl_lossy,ar_1:1,c_fill/http://res.cloudinary.com/demo/image/upload/bike.jpg" alt="image1" data-text="this is three"></div>
		<div class="content" data-legend="2nd legend"><img src="https://res.cloudinary.com/chriszak/image/fetch/q_auto,f_auto,fl_lossy,ar_1:1,c_fill,g_auto/http://res.cloudinary.com/demo/image/upload/bike.jpg" alt="image1" data-text="this is two"></div>
		<div class="content" data-legend="image 3"><a href="https://res.cloudinary.com/chriszak/image/fetch/q_auto,f_auto,fl_lossy,w_200,h_200,c_thumb/http://res.cloudinary.com/demo/image/upload/bike.jpg" target="_blank"><img src="https://res.cloudinary.com/chriszak/image/fetch/q_auto,f_auto,fl_lossy,w_200,h_200,c_thumb/http://res.cloudinary.com/demo/image/upload/bike.jpg" alt="image1" data-text="this is three"></a></div>	
	</div>
</body>
</html>
