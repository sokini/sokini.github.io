---
layout: page
title: Week 5 - Lecture
---

Order the loop so that it counts the number of empty spaces in a text\

Hint: The first two lines are:\
empty_space = " "\
number_of_spaces = 0 \ 
The last line is the print line and is not indented

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "empty_space = &quot; &quot;\n" +
    "number_of_spaces = 0\n" +
    "for character in input(&quot;Insert your sentence here: &quot;):\n" +
    "    if character == empty_space:\n" +
    "        number_of_spaces += 1\n" +
    "print(&quot;I found &quot; + str(number_of_spaces) + &quot; empty spaces in the text&quot;)";
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

## [Next](./week5_lec3.html)
## [Previous](./week5_lec1.html)
