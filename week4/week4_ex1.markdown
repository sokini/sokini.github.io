---
layout: page
title: Week 4 - Exercises
---

We attempted to create a program for calculating the factorial of a user-entered number. Unfortunately, our code got scrambled. Your task is to arrange the code blocks in the correct order so that the program outputs the factorials accurately.

Reminder:
The factorial of a non-negative integer n, denoted as n!, is the product of all positive integers up to n. 


<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "num = int(input("Enter a number: "))\n" +
    "factorial = 1\n" +
    "for i in range(1, num + 1):\n" +
    "factorial=factorial*i\n" +
    "    print("The factorial of " + str(num) + " is " + str(factorial))\n";
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

