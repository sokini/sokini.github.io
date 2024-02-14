---
layout: page
title: Week 3
---

The PDP lecture finished and you went to Analog to pick up a coffee before the exercise session. <br>
However, the line was looong and now you are rushing to get to fourth floor for exercises. <br>
Order the code for the ITU elevator asap, so you can make it to class in time!

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "current_floor = 0\n" +
    "destination_floor = current_floor + 4\n" +
    "current_floor = destination_floor\n" +
    "if (current_floor == 4):\n" +
    "	print(&quot;Welcome to 4th floor!&quot;)";
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

## [Previous](./week3_lec1.html)
## [Next](./week3_lec3.html)