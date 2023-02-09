---
layout: page
title: Week 2 - Exercises
---

This code was written to measure and update the size of our new dog as they go through their first years. A new measurement is made (in centimeters) 
every 5 months. Since we are storing the measurement in a variable that we want to update, we want to use the *'temp'* variable to make sure each time we do a measurement
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
  var initial = "last_biannual_measuremente = 78\n" +
    "current_measurement = 92\n" +
    "temp = last_biannual_measuremente\n" +
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

