---
layout: page
title: Week 3
---

Finally! Classes are done and you are heading home. <br>
Order the code below, so you can make it to the basement and pick up your bike. <br>
Don't forget your bike keys!

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "current_floor = 4\n" +
    "keys = True\n" +
    "destination_floor = current_floor - 5\n" +
    "current_floor = destination_floor\n" +
    "if (current_floor == -1 and keys == True):\n" +
    "	print(&quot;Welcome to the basement!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
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



## [Previous](./week3_lec2.html)
## [Next](./week3_lec4.html)
