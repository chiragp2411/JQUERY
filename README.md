<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>FAQ</title>
<link rel="stylesheet" type="text/css" href="FAQ_Main_CSS.css" />

<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js" type="text/javascript"></script>
<script type="text/javascript">
$(document).ready(function() {
	
	$(".answer").hide();
	$(".definition").hide();
	$("#login_form").hide();
	
	
	//$("h1").repeat(400).toggleClass(".change_head").overAndOver();
	
	//To display tooltip
	/*$(".question").hover(
	function(){
			var destination=$(this).offset();
			$(".definition").css({
				top:destination.top,
				left:destination.left
			});
		$(".definition").show();
		},
		function(){
			$(".definition").hide();
		}
		);*/
	
	//To display answer
	$(".question").toggle(
	function(event){		
		$(this).next(".answer").slideDown(300,"linear");
		$(this).addClass("closeAnswer");
	},
	function(event){		
		$(this).next(".answer").slideUp(300);
		$(this).removeClass("closeAnswer","linear");
	});

	//To display Login window
	$("#open").toggle(
	function(){
		$("#login_form").slideDown(400,"linear");	
		$(this).addClass("closeLogin");
	},
	function(){
		$("#login_form").slideUp(400,"linear");
		$(this).removeClass("closeLogin");
	}
	);
	
	//$("div:not(#login_form)").click(function(){$("#login_form").hide();})
	//$("body *").not("body #login_form").click(function(){$("#login_form").hide();});
	
  
});
</script>
</head>

<body>

<div id="header">
    <h1>A One Page FAQs</h1>
    
    <div id="login">
    	<div id="open">Login</div>
    	<div id="login_form">
        
        <form>
        	<input type="text" name="username" id="username" placeholder="Username">
            <input type="password" name="password" id="password" placeholder="Password">
            <input type="submit" name="submit" value="Sign In" id="submit">
        </form>    
       
        </div>
    </div>
    
</div>

<div id="FAQ">
    <div class="question">Why is Quora obsessed with Elon Musk?</div>
    <div class="answer">We all want to be inspired, to be hopeful and excited by the possibility of a better tomorrow. Elon Musk embodies the entrepreneurial spirit which says it's not good enough to hope for a better world without being committed to building it. We all have hopes, dreams and aspirations. So when we notice someone turning their vision into reality a part of us feels more alive, invigorated, and more open to possibilities. Musk's vision of the future speaks to our imagination because it is so courageous and audacious that it transcends'us'.Multi-Planetary life, sustainable energy and an inevitable move into gene manipulation and AI are exciting today...but they will be incredibly impactful tomorrow. In this way Musk is shaping a future for generations to come, and we intuitively know how important that is.</div><hr>
    
    <div class="question">What are some smart answers given to an interviewer?</div>
    <div class="answer">I’ve worked as a recruiter for the past 6 years or so and I’ll be happy to give you my opinions based on what I look for (and what I see other recruiters look for) in these answers. I think people get annoyed with the “common behavioral questions” but they are all asked for good reasons.</div><hr>
    
    
    <div class="question">What are some revolutionary ideas in making a city "smart"?</div>
    <div class="answer">I will answer your question with a question: What is a smart city operating system? If you mean a proprietary all-inclusive software or operating system, I would say that approach to large, messy concepts like "smart city" rarely works. I think more what is needed is open standards that will allow various smart systems to interact with each other. This will allow for progressive improvement and implementation, and is more likely to be secure and robust. The model is the internet, not Microsoft Office.</div><hr>
    
    <div class="question">Why do people ask dumb questions on Quora?</div>
    <div class="answer">I'm not sure what you consider to be a stupid question, but I often write long answers to questions some other people think are stupid. Why do I do it? Because I don't think they're stupid.So-called stupid questions are often naive questions, which means they're questions for which grownups are supposed to have a ready answer. This often means many people (myself included) haven't thought things through. They're just coming out with knee-jerk conventional responses. Most questions deepen when you examine each word and phrase in them and ponder their underlying assumptions.This tends to reveal hidden ambiguity, and what formerly seemed obvious is now clearly complex and nuanced. </div><hr>

<span class="definition">Click on the Question to hide/unhide the Answer</span>

</div>
</body>
</html>
