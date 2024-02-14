---
layout: page
title: Week 3
---

Just as you unlock your bike, you get a text from your study group, inviting you to join them in Scrollbar. <br>
Before venturing with the elevator to the ground floor, you want to make sure you can afford a pitcher for all of you. <br>

Order the code below, such that you only go up with the elevator, if you can afford a pitcher. <br>

Hints:
- Check your account as the first thing!<br>
- After this, if you can afford a pitcher,set the current_floor and destination_floor<br>
- Then, if you can afford a pitcher and the current_floor is ground floor, get off the elevator!

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "account = 100\n" +
    "if account &lt; 100:\n" +
    "can_afford_pitcher = False\n" +
    "elif account &ge; 100:\n" +
    "can_afford_pitcher = True\n" +
    "if can_afford_pitcher:\n" +
    "current_floor = -1\n" +    "destination_floor = current_floor + 1\n" +
    "current_floor = destination_floor\n" +
    "if current_floor == 0 and can_afford_pitcher == True:\n" +
    "	print(&quot;Cheers! And welcome to the ground floor!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## [Previous](./week3_lec3.html)

