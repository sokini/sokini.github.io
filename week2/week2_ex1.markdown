---
layout: page
title: Week 2 - Exercises
---

This code was designed to track and adjust the size of our recently acquired dog during its initial years. A new measurement, recorded in centimeters, is taken every 5 months. To ensure the continuous update of our measurement variable, we employ the 'temp' variable. Specifically, 'temp' is assigned the value of the last biannual measurement before the current one, and subsequently, the "last_biannual_measurement" variable is updated with the value of the current measurement. 

But - oh no - we just dropped our code and now it's all scrambled up :( help us find the correct order so that the code correctly outputs the latest and previous measurement.

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "last_biannual_measuremente = 78\n" +
    "current_measurement = 92\n" +
    "temp = last_biannual_measurement\n" +
    "last_biannual_measuremente = current_measurement\n" +
    "print(&quot;The last time the dog was measured, they were: &quot; + str(temp) + &quot;cm&quot;)\n" +
    "print(&quot;The last measured size is: &quot; + str(current_measurement) + &quot;cm&quot;)";
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

