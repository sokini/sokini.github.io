---
layout: page
title: Week 5 - Lecture
---

Arrange the following function for a simple calculator

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def simple_calculator(a, b):\n" +
    "    operation = input(&quot;What do you want to do? (choose between sum, minus, multiplication and division) \n&quot;)\n" +
    "    if operation == &quot;sum&quot;:\n" +
    "        return a + b\n" +
    "    elif operation == &quot;minus&quot;:\n" +
    "        return a - b\n" +
    "    elif operation == &quot;multiplication&quot;:\n" +
    "        return a * b\n" +
    "    elif operation == &quot;division&quot;:\n" +
    "        return a / b\n" +
    "    else:\n" +
    "        return print(&quot;The operation you selected is not implemented yet&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang:": "en",
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

## [Previous](./week5_lec3.html)
