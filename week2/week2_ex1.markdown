---
layout: page
title: Week 2 - Exercises
---

This code was written to measure and update the size of our new dog as they go through their first years. A new measurement is made (in centimeters) 
every 5 months. Since we are storing the measurement in a variable that we want to update, we want to use the *'tmp'* variable to make sure each time we do a measurement
the latest measurement is transfered to a variable that allows us to see how much the dog has grown in the past 5 months.

But we dropped our code and now it's all scrambled up :( help us find the correct order so that the code correctly outputs the latest and previous measurements.


<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "old_size = 78\n" +
    "new_size = 92\n" +
    "temp = old_size\n" +
    "old_size = new_size\n" +
    "new_size = temp\n" +
    "print(&quot;new size is&quot;, old_size)\n" +
    "print(&quot;archive: old size is &quot;, new_size)";
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
