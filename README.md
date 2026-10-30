<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Living in a Host Family — B1–B2</title>

<style>
:root {
--navy:#243453;
--blue:#5368c8;
--light:#edf0ff;
--green:#e5f5ed;
--bg:#f6f7fb;
--ink:#263249;
--muted:#68758a;
--line:#e4e8f0;
--white:#fff;
}
*{box-sizing:border-box}
body{
margin:0;
background:var(--bg);
color:var(--ink);
font:16px/1.6 Arial,sans-serif;
}
header{
background:linear-gradient(130deg,#233653,#586bca);
color:white;
padding:42px 20px;
}
header .wrap,main{max-width:1100px;margin:auto}
header h1{
font-size:clamp(2rem,5vw,3.4rem);
line-height:1.1;
margin:10px 0;
}
header p{max-width:750px;color:#edf0ff}
nav{
position:sticky;
top:0;
z-index:10;
display:flex;
gap:7px;
overflow-x:auto;
padding:10px max(12px,calc((100% - 1100px)/2));
background:#ffffffed;
border-bottom:1px solid var(--line);
}
nav a{
white-space:nowrap;
text-decoration:none;
color:var(--navy);
font-weight:bold;
padding:7px 12px;
border-radius:20px;
}
nav a:hover{background:var(--light)}
main{padding:25px 16px 60px}
section{scroll-margin-top:75px;margin:30px 0 48px}
h2{font-size:1.8rem;margin:5px 0}
h3{margin-top:5px}
.tag{
font-size:.75rem;
font-weight:800;
letter-spacing:.13em;
color:var(--blue);
}
.sub,.muted{color:var(--muted)}
.box,.task,.reading{
background:white;
border:1px solid var(--line);
border-radius:18px;
padding:20px;
margin:15px 0;
box-shadow:0 9px 28px #2534530c;
}
.tabs,.buttons,.options{
display:flex;
gap:8px;
flex-wrap:wrap;
}
button{
font:inherit;
}
.btn{
border:0;
border-radius:10px;
background:var(--light);
color:var(--blue);
font-weight:750;
padding:9px 14px;
cursor:pointer;
}
.btn:hover{filter:brightness(.97)}
.btn.primary{background:var(--blue);color:white}
.btn:disabled{opacity:.4}
.card{
height:285px;
max-width:650px;
margin:20px auto;
perspective:1000px;
cursor:pointer;
}
.inner{
height:100%;
position:relative;
transition:.5s;
transform-style:preserve-3d;
}
.card.flip .inner{transform:rotateY(180deg)}
.face{
position:absolute;
inset:0;
backface-visibility:hidden;
border-radius:22px;
border:1px solid var(--line);
box-shadow:0 12px 30px #25345317;
display:flex;
flex-direction:column;
align-items:center;
justify-content:center;
text-align:center;
padding:28px;
}
.front{background:linear-gradient(140deg,#fff,#edf0ff)}
.back{background:linear-gradient(140deg,#e2f4eb,#fff);transform:rotateY(180deg)}
.word{font-size:2rem;font-weight:900}
.definition{max-width:520px;color:#58647a;margin-top:15px}
.translation{font-size:1.8rem;font-weight:850}
.label{
font-size:.72rem;
letter-spacing:.13em;
color:var(--muted);
margin-bottom:12px;
}
.center{text-align:center}
.question{
border-top:1px solid var(--line);
padding:13px 0;
}
.question:first-child{border:0}
.options label{
background:#f4f5f9;
border:1px solid var(--line);
border-radius:9px;
padding:5px 9px;
cursor:pointer;
}
input[type=radio]{accent-color:var(--blue)}
input[type=text]{
font:inherit;
border:1px solid #d8deea;
border-radius:9px;
padding:8px 10px;
max-width:100%;
}
textarea{
font:inherit;
border:1px solid #d8deea;
border-radius:9px;
padding:10px;
width:100%;
min-height:90px;
}
.blank{width:min(260px,100%)}
.feedback{font-weight:800;margin-top:10px}
.good{color:#16835e}
.bad{color:#bd573f}
.quote{
background:#f3f5fc;
border-left:4px solid var(--blue);
padding:10px 14px;
margin:10px 0;
border-radius:0 9px 9px 0;
}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.note{background:#fff7e7;padding:13px;border-radius:10px}
.reading p{margin:13px 0}
footer{text-align:center;color:var(--muted);padding:25px}
@media(max-width:650px){
.grid{grid-template-columns:1fr}
.box,.task,.reading{padding:15px}
.card{height:270px}
}
</style>
</head>

<body>

<header>
<div class="wrap">
<small>ENGLISH LESSON · B1–B2</small>
<h1>Living in a Host Family</h1>
<p>
Vocabulary flashcards, reading, speaking and grammar practice.
Study the vocabulary, read the text and complete the interactive exercises.
</p>
</div>
</header>

<nav>
<a href="#cards">Vocabulary</a>
<a href="#attitudes">Attitudes</a>
<a href="#phrasals">Phrasal verbs</a>
<a href="#abroad">Study abroad</a>
<a href="#reading">Reading</a>
<a href="#usedto">Used to</a>
</nav>

<main>

<!-- VOCABULARY CARDS -->

<section id="cards">
<span class="tag">PART 1</span>
<h2>Vocabulary flashcards</h2>
<p class="sub">
Choose a vocabulary group. Click the card to see the Russian translation.
Use the arrows to move between cards.
</p>

<div class="box">
<div class="tabs" id="cardGroups"></div>

<div class="card" id="flashcard" tabindex="0">
<div class="inner">
<div class="face front">
<div class="label">WORD AND DEFINITION · CLICK TO FLIP</div>
<div class="word" id="cardWord"></div>
<div class="definition" id="cardDefinition"></div>
</div>

<div class="face back">
<div class="label">RUSSIAN TRANSLATION</div>
<div class="translation" id="cardTranslation"></div>
</div>
</div>
</div>

<div class="buttons center">
<button class="btn" id="previousCard">← Previous</button>
<b id="cardCounter"></b>
<button class="btn" id="nextCard">Next →</button>
</div>
</div>
</section>

<!-- ATTITUDE -->

<section id="attitudes">
<span class="tag">PART 2</span>
<h2>Attitude and tone of voice</h2>

<div class="task">
<h3>1. Guess the attitude</h3>
<p>Choose the adjective that best describes the speaker.</p>
<div id="attitudeQuiz"></div>
<button class="btn primary" onclick="checkQuiz('attitudeQuiz')">Check answers</button>
<div class="feedback" id="attitudeQuizFeedback"></div>
</div>

<div class="task">
<h3>2. One situation — different attitudes</h3>
<p>
Your host brother is 40 minutes late and has forgotten to tell you.
Rewrite your reaction in each tone.
</p>

<p><b>Sarcastic</b></p>
<textarea placeholder="Oh, fantastic..."></textarea>

<p><b>Aggressive</b></p>
<textarea></textarea>

<p><b>Calm</b></p>
<textarea></textarea>

<p><b>Sympathetic</b></p>
<textarea></textarea>

<p><b>Accusing</b></p>
<textarea></textarea>
</div>

<div class="task">
<h3>3. Listening strategy: read between the lines</h3>
<p>
Read each phrase aloud in two different tones. Explain how the speaker's
intention changes. Pay attention to the tone of voice.
</p>

<div class="quote">“That's just great.”</div>
<div class="quote">“You really should be more careful.”</div>
<div class="quote">“I'm sure everything will be fine.”</div>
<div class="quote">“We need to leave right now.”</div>

<p>
Which phrase could sound sarcastic? Which could have an urgent tone of voice?
Which could be giving a warning?
</p>
<textarea placeholder="Write your observations..."></textarea>
</div>

<div class="task">
<h3>4. Complete with an attitude adjective</h3>
<p class="muted">
bitter · complimentary · enthusiastic · grateful · miserable ·
nostalgic · optimistic · pessimistic · arrogant · urgent
</p>
<div id="attitudeFill"></div>
<button class="btn primary" onclick="checkFill('attitudeFill')">Check answers</button>
<div class="feedback" id="attitudeFillFeedback"></div>
</div>
</section>

<!-- PHRASAL VERBS -->

<section id="phrasals">
<span class="tag">PART 3</span>
<h2>Phrasal verbs</h2>

<div class="task">
<h3>5. Complete the story</h3>
<p class="muted">
live up to · walk out on · fit in with · get on with · sign up for ·
catch up with · go through with · put up with · run out of
</p>
<div id="phrasalStory"></div>
<button class="btn primary" onclick="checkFill('phrasalStory')">Check answers</button>
<div class="feedback" id="phrasalStoryFeedback"></div>
</div>

<div class="task">
<h3>6. Multiple choice</h3>
<div id="phrasalMCQ"></div>
<button class="btn primary" onclick="checkQuiz('phrasalMCQ')">Check answers</button>
<div class="feedback" id="phrasalMCQFeedback"></div>
</div>

<div class="task">
<h3>7. Same verb, different meaning</h3>
<p>Choose the correct phrasal verb.</p>
<div id="sameVerb"></div>
<button class="btn primary" onclick="checkQuiz('sameVerb')">Check answers</button>
<div class="feedback" id="sameVerbFeedback"></div>
</div>

<div class="task">
<h3>8. Replace the phrase with a phrasal verb</h3>
<ol>
<li>I really admire my older host sister. <input class="blank" data-answer="look up to"></li>
<li>We need to compensate for the time we lost. <input class="blank" data-answer="make up for"></li>
<li>He escaped from the hotel without saying goodbye. <input class="blank" data-answer="got away"></li>
<li>She broke her promise. <input class="blank" data-answer="went back on"></li>
<li>What do you usually do in your free time? <input class="blank" data-answer="get up to"></li>
<li>I searched for the word in an online dictionary. <input class="blank" data-answer="looked up"></li>
</ol>
</div>
</section>

<!-- STUDY ABROAD -->

<section id="abroad">
<span class="tag">PART 4</span>
<h2>Study abroad</h2>

<div class="task">
<h3>9. Advantages and disadvantages</h3>
<p>
Sort the phrases into the most suitable category. Some experiences can be
both positive and challenging, depending on the person.
</p>
<div class="grid">
<div><b>Potential advantages</b><div id="pros" class="drop"></div></div>
<div><b>Potential challenges</b><div id="cons" class="drop"></div></div>
</div>
<div id="sortItems" class="tabs"></div>
<button class="btn primary" onclick="checkSort()">Check sorting</button>
<div class="feedback" id="sortFeedback"></div>
</div>

<div class="task">
<h3>10. Complete the conversation</h3>
<p class="muted">
exchange programme · making new friends · missing home · gaining confidence ·
speaking a foreign language · visiting different places
</p>
<div id="abroadDialogue"></div>
<button class="btn primary" onclick="checkFill('abroadDialogue')">Check answers</button>
<div class="feedback" id="abroadDialogueFeedback"></div>
</div>

<div class="task">
<h3>11. What would you do if…?</h3>
<ol>
<li>You don't get on with your host family's teenage son.</li>
<li>You miss your family and friends so much that you want to return home.</li>
<li>You find it difficult to fit in with your new classmates.</li>
<li>Your host family eats food you really dislike.</li>
<li>You accidentally break an important house rule.</li>
<li>You can't understand an urgent warning because of the speaker's accent.</li>
</ol>
<textarea placeholder="Discuss and write possible solutions..."></textarea>
</div>

<div class="task">
<h3>12. What's the best response?</h3>
<div id="responseQuiz"></div>
<button class="btn primary" onclick="checkQuiz('responseQuiz')">Check answers</button>
<div class="feedback" id="responseQuizFeedback"></div>
</div>

<div class="task">
<h3>13. Vocabulary detective — four cases</h3>
<div id="detectiveQuiz"></div>
<button class="btn primary" onclick="checkQuiz('detectiveQuiz')">Check answers</button>
<div class="feedback" id="detectiveQuizFeedback"></div>
</div>

<div class="task">
<h3>14. Mini-essay</h3>
<p>
Write 150–180 words:
<b>Would you recommend living with a host family to someone taking part in an exchange programme?</b>
</p>
<p>Include at least 6 lesson vocabulary items, one challenge, one example of personal growth and a conclusion.</p>
<textarea id="essay"></textarea>
<p class="muted" id="wordCount">0 words</p>
</div>

<div class="task">
<h3>15. Agree or disagree?</h3>
<ol>
<li>Living with a host family is the best way to learn a foreign language.</li>
<li>Students should follow all the rules of their host family, even if they disagree.</li>
<li>Missing home is an unavoidable part of studying abroad.</li>
<li>Living abroad makes people more independent and open-minded.</li>
</ol>
<textarea placeholder="Support your opinions with arguments and examples..."></textarea>
</div>
</section>

<!-- READING -->

<section id="reading">
<span class="tag">PART 5</span>
<h2>Reading: Living in a Host Family</h2>

<article class="reading">
<h3>Living in a Host Family</h3>

<p>
When I decided to take part in an exchange programme in England, I knew that
living with a host family would be both exciting and challenging. I was
enthusiastic about the opportunity to speak a foreign language every day,
visit different places and make new friends. However, I was also a little
nervous because I had never lived with people I didn't know before.
</p>

<p>
My host family, the Browns, were very welcoming. They lived in a small town
not far from London. At first, I found it difficult to fit in with the
family. They had their own traditions, daily routines and rules. For
example, they always had dinner together at seven o'clock, and everyone was
expected to help with the housework. I wasn't used to this, but I tried to
be calm and positive.
</p>

<p>
One of the biggest challenges was eating different food. The Browns usually
had sandwiches, potatoes or meat for dinner, while I was used to eating
completely different meals at home. Sometimes I missed my family and
friends, and I felt a little miserable and nostalgic. Luckily, Mrs Brown
was very sympathetic. She always listened to me and tried to make me feel
better. I was grateful for her support.
</p>

<p>
Communication was another challenge. Although I had studied English for
several years, I sometimes couldn't understand the Browns because of their
accents or the way they spoke. I learned that sometimes the words alone do
not fully express the speaker's intention. It is important to pay attention
to the tone of voice. For example, an urgent tone of voice can mean that
someone needs help immediately, while a sarcastic tone can mean the opposite
of what the person actually says.
</p>

<p>
After a few weeks, things became easier. I started to get on with everyone
in the family, especially their teenage daughter, Emily. We often watched
films together and talked about school, music and our hobbies. I also gained
confidence and became less afraid of making mistakes when speaking English.
</p>

<p>
Living in a host family taught me to be more independent, patient and
open-minded. Of course, there were moments when I wanted to walk out on the
experience and go back home, but I'm glad I didn't. I learned that adapting
to a new culture takes time, and that small difficulties can lead to
valuable experiences. Looking back, I feel optimistic about the future and
would definitely recommend living with a host family to other students.
</p>
</article>

<div class="task">
<h3>16. True or False?</h3>
<div id="readingTF"></div>
<button class="btn primary" onclick="checkQuiz('readingTF')">Check answers</button>
<div class="feedback" id="readingTFFeedback"></div>
<p class="muted">Correct the false statements orally or in your notebook.</p>
</div>

<div class="task">
<h3>17. Find the words and phrases</h3>
<p>Find an expression in the text matching each definition.</p>
<div id="readingFind"></div>
<button class="btn primary" onclick="checkFill('readingFind')">Check answers</button>
<div class="feedback" id="readingFindFeedback"></div>
</div>

<div class="task">
<h3>18. Discussion</h3>
<ol>
<li>What are the advantages of living in a host family?</li>
<li>What difficulties might a student experience when living abroad?</li>
<li>How can a host family help a foreign student feel comfortable?</li>
<li>Why is it important to pay attention to the tone of voice?</li>
<li>What would you do if you didn't get on with your host family?</li>
<li>Would you prefer to live with a host family or in a student residence? Why?</li>
</ol>
<p>Use at least five expressions from the text.</p>
<textarea placeholder="Write your answers..."></textarea>
</div>
</section>

<!-- USED TO -->

<section id="usedto">
<span class="tag">PART 6</span>
<h2>Grammar focus: USED TO</h2>

<div class="box">
<h3>Grammar reminder</h3>
<p><b>used to + infinitive</b> — past habits or states that are no longer true:</p>
<p><i>I used to live with my parents.</i></p>

<p><b>would + infinitive</b> — repeated past actions, not usually states:</p>
<p><i>We would have dinner together every Sunday.</i></p>

<p><b>be used to + noun / -ing</b> — be accustomed to something:</p>
<p><i>I'm used to sharing a room.</i></p>

<p><b>get used to + noun / -ing</b> — become accustomed to something:</p>
<p><i>I'm getting used to speaking English every day.</i></p>

<div class="note">
After <b>didn't</b>, use <i>use to</i>.
After <b>be/get used to</b>, use a noun or an <i>-ing</i> form.
</div>
</div>

<div class="task">
<h3>19. Advanced transformations</h3>
<p>Rewrite the sentences using the word in brackets. Do not change the meaning.</p>
<div id="usedTransform"></div>
<button class="btn primary" onclick="checkFill('usedTransform')">Check answers</button>
<div class="feedback" id="usedTransformFeedback"></div>
</div>

<div class="task">
<h3>20. Find and correct the mistakes</h3>
<p>Each sentence contains one grammar mistake. Rewrite it correctly.</p>
<div id="usedErrors"></div>
<button class="btn primary" onclick="checkFill('usedErrors')">Check answers</button>
<div class="feedback" id="usedErrorsFeedback"></div>
</div>

<div class="task">
<h3>21. Complete the story</h3>
<p>Use used to, would, be used to or get used to. Change the form where necessary.</p>
<div id="usedStory"></div>
<button class="btn primary" onclick="checkFill('usedStory')">Check answers</button>
<div class="feedback" id="usedStoryFeedback"></div>
</div>

<div class="task">
<h3>22. Explain the difference</h3>
<p>Explain the difference in meaning in each group. Then write your own example.</p>

<div class="quote">
<b>A</b> I used to share a room. / I am used to sharing a room. /
I am getting used to sharing a room.
</div>
<div class="quote">
<b>B</b> My host family would invite their neighbours for dinner. /
My host family used to invite their neighbours for dinner.
</div>
<div class="quote">
<b>C</b> I used to be very shy. / I would be very shy.
</div>
<div class="quote">
<b>D</b> I didn't use to cook. / I wasn't used to cooking. /
I couldn't get used to cooking.
</div>
<div class="quote">
<b>E</b> There used to be strict rules in the house. /
I used to follow strict rules in the house.
</div>

<textarea placeholder="Explain and write your examples..."></textarea>
</div>

<div class="task">
<h3>23. Speaking challenge: Life before and after moving abroad</h3>
<p>
Imagine you spent a year abroad and lived with a host family. Talk about
your daily routine, eating habits, housework, relationships, confidence,
free time and attitude towards other cultures.
</p>
<p><b>Requirements:</b></p>
<ul>
<li>At least 3 sentences with <i>used to</i>.</li>
<li>2 sentences with <i>would</i>.</li>
<li>2 sentences with <i>be used to</i>.</li>
<li>2 sentences with <i>get used to</i>.</li>
<li>One negative sentence and one question.</li>
</ul>
<textarea placeholder="Plan or write your response..."></textarea>
</div>

</section>
</main>

<footer>English B1–B2 · Living in a Host Family</footer>

<script>
// VOCABULARY DATA
const vocabulary = {
"Attitude adjectives":[
["calm","Not showing strong emotions; relaxed and in control.","спокойный"],
["complimentary","Expressing praise or admiration.","делающий комплименты; хвалебный"],
["enthusiastic","Showing a lot of interest, excitement or energy.","восторженный; полный энтузиазма"],
["grateful","Feeling or showing thanks for something.","благодарный"],
["accusing","Suggesting that someone has done something wrong.","обвиняющий"],
["aggressive","Behaving in an angry or forceful way.","агрессивный"],
["arrogant","Thinking that you are better or more important than other people.","высокомерный"],
["bitter","Feeling angry or disappointed because of an unfair or unpleasant experience.","озлобленный; испытывающий горечь"],
["miserable","Very unhappy or uncomfortable.","несчастный; подавленный"],
["pessimistic","Expecting bad things to happen.","пессимистичный"],
["sarcastic","Using words that mean the opposite of what you really want to say, often to criticise or mock.","саркастичный"],
["nostalgic","Feeling happy and slightly sad when remembering the past.","испытывающий ностальгию"],
["optimistic","Expecting good things to happen.","оптимистичный"],
["sympathetic","Showing that you understand and care about someone else's problems.","сочувствующий"],
["urgent","Needing immediate attention or action.","срочный; неотложный"]
],

"Listening & tone":[
["tone of voice","The way someone's voice sounds, which can show their feelings or attitude.","тон голоса"],
["an urgent tone of voice","A way of speaking that shows something needs to happen immediately.","срочная, настойчивая интонация"],
["giving a warning","Telling someone about possible danger or a problem.","предупреждение; предупреждать"],
["speaker's intention","What a person really wants to communicate or achieve by speaking.","намерение говорящего"],
["pay attention to","To listen to or watch something carefully.","обращать внимание на"],
["Sometimes, the words alone do not fully express the speaker's intention.","The literal words may not show exactly what the speaker means.","Иногда одни только слова не полностью передают намерение говорящего."]
],

"Phrasal verbs — Benjamin Button":[
["live up to","To be as good as someone expected.","соответствовать ожиданиям"],
["walk out on","To leave someone or something suddenly, especially when they need you.","бросить; уйти, оставив кого-либо"],
["fit in with","To feel that you belong to a group or are accepted by it.","вписываться; соответствовать"],
["get on with","To have a friendly relationship with someone.","ладить с кем-либо"],
["sign up for","To put your name on a list to take part in something.","записаться на; зарегистрироваться"],
["catch up with","To reach the same level or position as someone; to do something you have not had time to do.","догнать; наверстать"],
["go through with","To do something you have planned or promised, even if it is difficult.","довести до конца; выполнить, несмотря на трудности"],
["put up with","To accept an unpleasant situation or person without complaining.","терпеть; мириться с"],
["run out of","To have no more of something because it has all been used.","израсходовать; остаться без"]
],

"More phrasal verbs":[
["look up","To search for information in a book, dictionary or online.","искать информацию; смотреть в словаре"],
["look up to","To admire and respect someone.","восхищаться; уважать"],
["make up","To invent a story or excuse; also, to become friends again after an argument.","выдумывать; мириться"],
["make up for","To do something good to compensate for something bad or missed.","компенсировать; возмещать"],
["get away","To escape or leave a place.","сбежать; уехать"],
["get away with","To do something wrong without being punished.","избежать наказания за"],
["get up","To get out of bed; to stand up.","вставать"],
["get up to","To do something, often something unusual or naughty.","заниматься чем-либо; вытворять"],
["go in","To enter a place.","войти"],
["go in for","To like or take part in an activity; to have an interest in it.","увлекаться; заниматься"],
["go back","To return to a place or situation.","вернуться"],
["go back on","To fail to keep a promise or agreement.","нарушить обещание; отказаться от своих слов"]
],

"Study abroad":[
["exchange programmes","Arrangements that allow students to study in another country for a period of time.","программы обмена"],
["eating different food","Trying meals and dishes that are unfamiliar to you.","пробовать непривычную еду"],
["gaining confidence","Becoming more sure of your abilities.","обретение уверенности"],
["going to a different school","Studying at a school that is not your usual one.","переход в другую школу"],
["making new friends","Developing friendships with people you have recently met.","знакомство и приобретение новых друзей"],
["missing family/friends/home","Feeling sad because people and places you love are far away.","скучать по семье / друзьям / дому"],
["speaking a foreign language","Communicating in a language that is not your own.","говорить на иностранном языке"],
["visiting different places","Going to see a variety of locations.","посещать разные места"],
["watching foreign TV programmes","Viewing television shows made in another country or language.","смотреть иностранные телепередачи"]
]
};

let currentGroup=Object.keys(vocabulary)[0];
let currentIndex=0;

function renderGroups(){
const container = document.getElementById("cardGroups");

// Очищаем список кнопок
container.innerHTML = "";

// Создаём отдельную кнопку для каждой категории
Object.keys(vocabulary).forEach(group => {
const button = document.createElement("button");

button.type = "button";
button.className = "btn";

// Подсвечиваем активную категорию
if (group === currentGroup) {
button.classList.add("primary");
}

button.textContent = group;

// Переключаем категорию при нажатии
button.addEventListener("click", () => {
currentGroup = group;
currentIndex = 0;

renderGroups();
renderCard();
});

container.appendChild(button);
});
}

function renderCard(){
const item=vocabulary[currentGroup][currentIndex];
document.getElementById("cardWord").textContent=item[0];
document.getElementById("cardDefinition").textContent=item[1];
document.getElementById("cardTranslation").textContent=item[2];
document.getElementById("cardCounter").textContent=(currentIndex+1)+" / "+vocabulary[currentGroup].length;
document.getElementById("flashcard").classList.remove("flip");
}
document.getElementById("flashcard").onclick=()=>document.getElementById("flashcard").classList.toggle("flip");
document.getElementById("flashcard").onkeydown=e=>{
if(e.key==="Enter"||e.key===" "){e.preventDefault();document.getElementById("flashcard").classList.toggle("flip")}
};
document.getElementById("previousCard").onclick=()=>{
currentIndex=(currentIndex+vocabulary[currentGroup].length-1)%vocabulary[currentGroup].length;renderCard();
};
document.getElementById("nextCard").onclick=()=>{
currentIndex=(currentIndex+1)%vocabulary[currentGroup].length;renderCard();
};
renderGroups();renderCard();

// GENERAL INTERACTIVE TASK FUNCTIONS
function makeQuiz(id,data){
document.getElementById(id).innerHTML=data.map((q,i)=>`
<div class="question">
<b>${i+1}. ${q[0]}</b>
<div class="options">${q[1].map((option,j)=>`
<label><input type="radio" name="${id}_${i}" data-correct="${j===q[2]}"> ${option}</label>
`).join("")}</div></div>`).join("");
}
function makeFill(id,data){
document.getElementById(id).innerHTML=data.map((q,i)=>`
<div class="question">${i+1}. ${q[0]}
<input type="text" class="blank" data-answer="${q[1]}" placeholder="Your answer">
</div>`).join("");
}
function checkQuiz(id){
const questions=[...document.querySelectorAll("#"+id+" .question")];
let score=0;
questions.forEach(q=>{
const answer=q.querySelector("input:checked");
if(answer && answer.dataset.correct==="true")score++;
});
const feedback=document.getElementById(id+"Feedback");
feedback.className="feedback "+(score===questions.length?"good":"bad");
feedback.textContent=`Correct answers: ${score} / ${questions.length}`;
}
function normalise(s){
return s.toLowerCase().trim().replace(/[.,!?']/g,"").replace(/\s+/g," ");
}
function checkFill(id){
const inputs=[...document.querySelectorAll("#"+id+" input[data-answer]")];
let score=0;
inputs.forEach(input=>{
const accepted=input.dataset.answer.split("|").map(normalise);
const correct=accepted.includes(normalise(input.value));
if(correct)score++;
input.style.borderColor=correct?"#16835e":"#bd573f";
});
const feedback=document.getElementById(id+"Feedback");
feedback.className="feedback "+(score===inputs.length?"good":"bad");
feedback.textContent=`Correct answers: ${score} / ${inputs.length}. Some open answers may have other acceptable versions.`;
}

// ATTITUDE QUIZ
makeQuiz("attitudeQuiz",[
["“I can’t believe you remembered my birthday. Thank you so much!”",["grateful","aggressive","pessimistic"],0],
["“Oh, brilliant. Another three hours at the airport. Just what I wanted.”",["complimentary","sarcastic","calm"],1],
["“I’m sure you’ll settle in and make friends soon.”",["optimistic","bitter","accusing"],0],
["“You never listen to anything I say!”",["nostalgic","accusing","sympathetic"],1],
["“I understand that you miss home. It must be difficult.”",["arrogant","sympathetic","aggressive"],1],
["“We need to leave immediately. The last bus is coming!”",["urgent","miserable","complimentary"],0],
["“Nobody here is as clever as I am.”",["grateful","arrogant","calm"],1],
["“Those old family photos remind me of my childhood.”",["nostalgic","pessimistic","aggressive"],0]
]);

makeFill("attitudeFill",[
["I felt very ______ when my host parents praised my progress.","grateful"],
["He made a ______ comment and said my presentation was excellent.","complimentary"],
["She was ______ about the exchange and couldn’t wait to leave.","enthusiastic"],
["His ______ attitude made him expect the worst.","pessimistic"],
["The message sounded ______: we had to call the school immediately.","urgent"],
["She felt ______ after the argument and refused to speak.","bitter"],
["I became ______ whenever I looked at photos of home.","nostalgic"],
["Despite the difficulties, he remained ______.","optimistic"],
["The student sounded ______ and complained constantly.","miserable"],
["The speaker was ______ and shouted at everyone.","aggressive"]
]);

// PHRASAL VERBS
makeFill("phrasalStory",[
["The film did not ______ the high expectations.","live up to"],
["He promised he would never ______ his family.","walk out on"],
["It took her a while to ______ her new classmates.","fit in with"],
["I really ______ my host parents.","get on with"],
["I decided to ______ a weekend photography course.","sign up for"],
["After missing lessons, I had to ______ the rest of the class.","catch up with"],
["She decided to ______ her plan to study abroad.","go through with"],
["I don’t know how you ______ that noise every night.","put up with"],
["We had to stop cooking because we had ______ milk.","run out of"]
]);

makeQuiz("phrasalMCQ",[
["I really ______ my English teacher.",["look up","look up to","look for"],1],
["You can ______ the meaning in a dictionary.",["look up","look up to","look after"],0],
["He invented an excuse; he ______ the whole story.",["made up","made up for","got away"],0],
["She worked extra hours to ______ the time she had missed.",["make up","make up for","get away with"],1],
["The teenager tried to ______ from the crowded room.",["get away","get away with","get up to"],0],
["He cheated but didn’t ______ it.",["get away","get away with","go in"],1],
["What did you ______ while we were away?",["get up to","get up","go back"],0],
["I usually ______ at 6.30.",["get up","get away","go in for"],0],
["My host brother ______ basketball.",["goes in","goes in for","goes back on"],1],
["She promised to help, but then she ______ her word.",["went back","went back on","went in"],1]
]);

makeQuiz("sameVerb",[
["I need to ______ the train timetable online.",["look up","look up to"],0],
["Younger students ______ older exchange students.",["look up","look up to"],1],
["He had to ______ an excuse.",["make up","make up for"],0],
["I’ll ______ missing your birthday by taking you out.",["make up","make up for"],1],
["The children tried to ______ from the crowded room.",["get away","get away with"],0],
["You can’t ______ breaking the rules.",["get away","get away with"],1],
["What time do you ______ on weekdays?",["get up","get up to"],0],
["What did you ______ at the weekend?",["get up","get up to"],1],
["Please ______ and close the door.",["go in","go in for"],0],
["Do you ______ any particular sport?",["go in","go in for"],1],
["We decided to ______ to our hometown.",["go back","go back on"],0],
["Never ______ a promise.",["go back","go back on"],1]
]);

// STUDY ABROAD SORTING
const sortData=[
["gaining confidence","pros"],
["making new friends","pros"],
["visiting different places","pros"],
["speaking a foreign language","pros"],
["watching foreign TV programmes","pros"],
["eating different food","cons"],
["missing family and friends","cons"],
["going to a different school","cons"]
];
function renderSort(){
document.getElementById("sortItems").innerHTML=sortData.map((item,i)=>
`<button class="btn" onclick="placeSort(${i})">${item[0]}</button>`
).join("");
}
function placeSort(i){
const choice=prompt("Enter A for advantage or C for challenge");
if(!choice)return;
const target=choice.toUpperCase()==="A"?"pros":"cons";
const old=document.querySelector('[data-sort="'+i+'"]');
if(old)old.remove();
const el=document.createElement("span");
el.className="pill";
el.dataset.sort=i;
el.textContent=sortData[i][0];
document.getElementById(target).appendChild(el);
}
function checkSort(){
let score=0;
document.querySelectorAll("[data-sort]").forEach(el=>{
if(el.parentElement.id===sortData[Number(el.dataset.sort)][1])score++;
});
document.getElementById("sortFeedback").textContent=
`Correct placements: ${score} / ${sortData.length}. Some experiences may be both positive and challenging.`;
}
renderSort();

makeFill("abroadDialogue",[
["Why did you apply for an ______? You wanted to study in another country.","exchange programme"],
["What was the best part? Probably ______. I still keep in touch with them.","making new friends"],
["Was it difficult? Yes, especially ______. I missed my parents.","missing home"],
["Did your English improve? Definitely, especially ______.","speaking a foreign language"],
["Did you become more independent? Yes, I was ______ too.","gaining confidence"],
["What did you do at weekends? We enjoyed ______ around the country.","visiting different places"]
]);

makeQuiz("responseQuiz",[
["Your host mother asks if everything is OK.",["It’s none of your business.","Thank you for asking. I’m just missing home a little.","You always ask silly questions."],1],
["Your host brother says the train leaves in ten minutes.",["No rush, let’s have tea.","I can see it’s urgent. Let me get my coat.","That’s complimentary."],1],
["You accidentally break a house rule.",["I’m sorry. I didn’t realise. I won’t do it again.","You should be grateful.","I’ll walk out on the family."],0],
["A classmate makes a sarcastic comment.",["Assume the literal meaning.","Pay attention to tone of voice and context.","Immediately become aggressive."],1]
]);

makeQuiz("detectiveQuiz",[
["“I thought living abroad would be easy, but it has been harder than expected.”",["Pessimistic","Complimentary","Urgent"],0],
["“You’ve made so much progress with your English!”",["Giving a warning","Making a complimentary comment","Being aggressive"],1],
["“I’m not angry. I just think it’s interesting you forgot again.”",["Sarcastic","Enthusiastic","Calm"],0],
["“Call the host parent immediately; there has been an accident.”",["Nostalgic tone","Urgent tone of voice","Pessimistic attitude"],1]
]);

// READING TASKS
makeQuiz("readingTF",[
["The student had lived with a host family before.",["True","False"],1],
["The Browns expected everyone to help with housework.",["True","False"],0],
["The student immediately enjoyed English food.",["True","False"],1],
["Mrs Brown was sympathetic and supportive.",["True","False"],0],
["The student found it easy to understand the Browns from the beginning.",["True","False"],1],
["Emily and the student became friends.",["True","False"],0],
["By the end, the student had gained confidence.",["True","False"],0],
["The student regrets taking part in the exchange.",["True","False"],1]
]);

makeFill("readingFind",[
["To become part of a group and feel accepted.","fit in with"],
["To feel thankful for something.","grateful"],
["To feel sad because you are far from home or the past.","nostalgic"],
["To have a friendly relationship with someone.","get on with"],
["To become more sure of your abilities.","gained confidence|gain confidence"],
["A programme that lets students study abroad.","exchange programme"],
["To listen or watch something carefully.","pay attention to"],
["Expecting good things to happen.","optimistic"],
["Showing that you understand and care about someone's problems.","sympathetic"],
["To leave someone or something suddenly.","walk out on"]
]);

// USED TO TASKS
makeFill("usedTransform",[
["When I was younger, I regularly spent my summers at my grandparents’ house. (USED)","I used to spend my summers at my grandparents house"],
["At first, sharing a room felt strange, but now it seems completely normal. (USED)","I am used to sharing a room"],
["My host family had breakfast together every Sunday. (WOULD)","My host family would have breakfast together every Sunday"],
["I didn’t enjoy speaking English all day at first, but now it is not difficult. (USED)","I am used to speaking English all day now|I have got used to speaking English all day"],
["In the past, I didn’t care much about other people’s routines. (USE)","I didn’t use to care much about other people’s routines"],
["It took me several weeks to feel comfortable with the family’s strict rules. (GOT)","I got used to the family’s strict rules"],
["My host mother cooked traditional meals every Friday. (WOULD)","My host mother would cook traditional meals every Friday"],
["I no longer feel uncomfortable when people speak very quickly. (USED)","I am used to people speaking very quickly"]
]);

makeFill("usedErrors",[
["I am used to wake up early.","I am used to waking up early"],
["When I lived in Spain, I would have a small bedroom of my own.","When I lived in Spain, I used to have a small bedroom of my own"],
["She didn’t used to enjoy foreign food.","She didn’t use to enjoy foreign food"],
["It took me a long time to used to speaking English.","It took me a long time to get used to speaking English"],
["My host family used to going on trips.","My host family used to go on trips"],
["I am getting used to live with different people.","I am getting used to living with different people"],
["There used to be a large garden behind the house.","There used to be a large garden behind the house"],
["When we were children, we would believe our parents knew everything.","When we were children, we used to believe our parents knew everything"]
]);

makeFill("usedStory",[
["I (live) with my parents, so sharing a house with strangers was new.","used to live"],
["My host family (have) dinner together every evening.","would have"],
["At first, I (not enjoy) these conversations.","didn’t use to enjoy|did not use to enjoy"],
["The family also (go) hiking every Sunday.","would go"],
["After a few weeks I (look forward) to these trips.","used to look forward to"],
["I (not be) independent before I moved abroad.","wasn’t used to being|was not used to being"],
["It took me time to (live) without my parents’ help.","get used to living"],
["By the end, I (feel) much more confident about living abroad.","had got used to feeling|had gotten used to feeling"]
]);

// ESSAY WORD COUNT
document.getElementById("essay").addEventListener("input",e=>{
const text=e.target.value.trim();
const count=text?text.split(/\s+/).length:0;
document.getElementById("wordCount").textContent=count+" words";
});
</script>
</body>
</html>
