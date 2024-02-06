---
layout: page
title: Week 2 - Exercise 2
---

Rearrange the code blocks to create a program that checks whether a given number is positive, negative, or zero and prints the result.

No need to use all the lines of code...

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "number1 = 3\n" +
    "current_measurement = 92 #distractor\n" +
    "is_positive = number1 > 0\n" +
    "is_negative = number1 < 0\n" +
    "is_zero = number1 == 0\n" +
    "print(&quot;Positive:&quot;, is_positive)\n"
    "print(&quot;Negative:&quot;, is_negative)\n" +
    "print(&quot;Zero:&quot;, is_zero)"
    ;
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

## [Bonus](./bonus_ex.html)
