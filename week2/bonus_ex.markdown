---
layout: page
title: Week 2 - Exercises Bonus!!
---

> You have decided to get into the lemonade stand business now that you are more familiar with IT systems. Unlike the other kids in the block, you actually use
> a book keeping system to keep track of your sales. Even better, you are writing this bookkeeping system yourself in Python. So far things have been quite easy, but
> competition from the other kids has gotten more and more tricky.

> To inject more revenue stream into your lemonda stand business you have decided to start selling Ice Tea. And it's going very well! But you noticed your
> book keeping system was only written to deal with one type of drink. Furthermore, now that you sell different drinks you want to keep track of your total drinks sales

Sadly on your way to implement the code you dropped it again 🤦 and it got jumbled up. Using it side-by-side with Mu Editor, make sure the code below works.




<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "lemonade = 10\n" +
    "iced_tea = 5\n" +
    "temp = lemonade\n" +
    "lemonade = 7\n" +
    "total_drinks = lemonade + iced_tea\n" +
    "print(&quot;Before selling:&quot;, total_drinks + temp)";
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
