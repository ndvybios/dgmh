$('.question-rankings').each(function(){
var index = Math.floor(Math.random() * 2 + 3);
var choice = $(this).find('input').get(index);
if(choice) {choice.checked = true;}
});
$('.question-answers').each(function(){
var index = Math.floor(Math.random() * 2 + 3);
var choice = $(this).find('input').get(index);
if(choice) { choice.checked = true; }
});
$('.section-questions').children("li").find('textarea').each(function(){
	$(this).context.value = "Không có";
});
for (i=0; i < 8; i++) {nextSection(); }

saveSurvey(true, function () { });
document.getElementById("btnBackToList").click();
