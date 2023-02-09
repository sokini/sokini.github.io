---
layout: page
title: Week 3
---

> Use all lines
> line 0 is destination = 0
> line 1 is current_station = 0
> line 2 is money = 100

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "destination = 0\n" +
    "current_station = 0\n" +
    "money = 100\n" +
    "destination = destination + 1\n" +
    "current_station = destination\n" +
    "if (money &lt; 100):\n" +
    "    ticket = False\n" +
    "elif (money == 100):\n" +
    "    ticket = True\n" +
    "if (current_station == 1 and ticket == True):\n" +
    "	print(&quot;Welcome to Mars!&quot;)";
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

## [Previous](./week3_lec3.html)

