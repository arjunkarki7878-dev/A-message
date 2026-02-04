# A-message
message from special person 🥀
<!DOCTYPE html><html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>💍 Proposal for Chasmiss 💖</title>
<style>
  body {
    margin: 0;
    height: 100vh;
    font-family: "Poppins", sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    background: radial-gradient(circle at top, #ff9a9e, #fad0c4);
    overflow: hidden;
  }
  .card {
    background: white;
    padding: 35px 30px;
    border-radius: 24px;
    text-align: center;
    box-shadow: 0 25px 50px rgba(0,0,0,0.25);
    max-width: 360px;
    animation: pop 0.7s ease;
    position: relative;
    z-index: 10;
  }
  @keyframes pop {
    from { transform: scale(0.85); opacity: 0; }
    to { transform: scale(1); opacity: 1; }
  }
  h1 { color: #ff4d6d; margin-bottom: 12px; }
  p { color: #555; line-height: 1.6; margin-bottom: 25px; }
  .hint { font-size: 14px; color: #999; }
  .buttons { display: flex; justify-content: center; gap: 14px; margin-top: 15px; }
  button { border: none; padding: 12px 22px; font-size: 16px; border-radius: 30px; cursor: pointer; transition: 0.3s; }
  .yes { background: #ff4d6d; color: white; }
  .no { background: #eee; color: #333; }
  .heart, .confetti, .firework, .cuteGif, .ring, .loveText {
    position: absolute;
    z-index: 5;
  }
  .cuteGif { width: 100px; border-radius: 12px; }
  .ring { width: 60px; animation: spin 2s linear infinite; }
  @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
  .loveText { font-size: 28px; color: #ff3366; font-weight: bold; text-shadow: 1px 1px 4px #fff; }
</style>
</head>
<body>
<div class="card" id="card">
  <h1>Hey Chasmiss 💕</h1>
  <p>Tap anywhere…<br>There’s something special I want to tell you.</p>
  <div class="hint">(touch the screen)</div>
</div>
<audio id="romanticMusic" loop>
  <source src="https://assets.mixkit.co/music/preview/mixkit-romantic-love-132.mp3" type="audio/mpeg">
</audio>
<script>
const card = document.getElementById("card");
let stepIndex = 0;
const music = document.getElementById("romanticMusic");const steps = [ {title: "Chasmiss ❤️", text: "From the moment you walked into my life, everything felt brighter."}, {title: "My Favorite Person 🌸", text: "Your smile, your laugh, the way you exist… it all means more to me than I can explain."}, {title: "Through Everything 💫", text: "I want to choose you on the good days, the hard days, and all the ordinary days in between."}, {title: "So Here’s My Question 💍", text: "Not just for today… but for forever."} ];

document.body.addEventListener("click", () => { if(stepIndex < steps.length){ card.innerHTML = <h1>${steps[stepIndex].title}</h1><p>${steps[stepIndex].text}</p><div class="hint">(touch again)</div>; stepIndex++; } else if(stepIndex === steps.length){ showMarriageQuestion(); stepIndex++; } if(music.paused) music.play(); });

function showMarriageQuestion(){ card.innerHTML = <h1>💖 Chasmiss 💖</h1><p>Will you marry me?</p><div class="buttons"><button class="yes">YES 💍</button><button class="no">NO 🙄</button></div>; const yesBtn = document.querySelector(".yes"); const noBtn = document.querySelector(".no"); const noMessages = ["Are you sure? 😳","Think again 😏","Don’t break my heart 💔","This is destiny 💘"]; let i=0; noBtn.addEventListener("click",()=>{ noBtn.textContent=noMessages[i%noMessages.length]; i++; const size=parseFloat(getComputedStyle(yesBtn).fontSize); yesBtn.style.fontSize=${size*1.4}px; }); yesBtn.addEventListener("click",()=>{ showCelebration(); }); }

function showCelebration(){ card.innerHTML = <h1>🎉 SHE SAID YES!!! 🎉</h1><p>You just made me the happiest person alive 🥰</p><p>Forever starts now ❤️</p>;

// Add Love Text const love = document.createElement('div'); love.className = 'loveText'; love.textContent = 'I LOVE YOU 💋'; love.style.top = '30%'; love.style.left = '50%'; love.style.transform = 'translateX(-50%)'; document.body.appendChild(love);

// Add Cute GIFs (kitten + rabbit + puppy) const gifs = [ 'https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif', 'https://media.giphy.com/media/Lq0h93752f6J9tijrh/giphy.gif', 'https://media.giphy.com/media/3o6Zt481isNVuQI1l6/giphy.gif' ]; gifs.forEach((src,i)=>{ const g=document.createElement('img'); g.src=src; g.className='cuteGif'; g.style.top=(20+30i)+'%'; g.style.left=(10+30i)+'%'; document.body.appendChild(g); });

// Add spinning ring const ring=document.createElement('img'); ring.src='https://upload.wikimedia.org/wikipedia/commons/thumb/6/6a/Ring_icon.svg/120px-Ring_icon.svg.png'; ring.className='ring'; ring.style.top='50%'; ring.style.left='80%'; document.body.appendChild(ring);

// Fireworks setInterval(createFirework, 400); }

function createFirework(){ const fw=document.createElement('div'); fw.className='firework'; fw.textContent='🎆'; fw.style.left=Math.random()*100+'vw'; fw.style.fontSize=(20+Math.random()*30)+'px'; fw.style.top=Math.random()*50+'vh'; document.body.appendChild(fw); setTimeout(()=>fw.remove(),1500); }

// Floating hearts setInterval(()=>{ const heart=document.createElement('div'); heart.className='heart'; heart.textContent='💖'; heart.style.left=Math.random()*100+'vw'; heart.style.fontSize=(20+Math.random()*20)+'px'; heart.style.top='100vh'; heart.style.transition='all 5s linear'; document.body.appendChild(heart); setTimeout(()=>{ heart.style.top='-10vh'; heart.style.opacity=0; },50); setTimeout(()=>heart.remove(),5500); },300);

// Confetti setInterval(()=>{ const conf=document.createElement('div'); conf.className='confetti'; conf.textContent='🎊'; conf.style.left=Math.random()*100+'vw'; conf.style.fontSize=(20+Math.random()*20)+'px'; conf.style.top='0vh'; conf.style.transition='all 4s linear'; document.body.appendChild(conf); setTimeout(()=>{ conf.style.top='100vh'; conf.style.opacity=0; },50); setTimeout(()=>conf.remove(),4000); },200); </script>

</body>
</html>
