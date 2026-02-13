let currentSlide = 0;
const slides = document.querySelectorAll('.slide');

function showSlide(n){
  slides.forEach(s => s.classList.remove('active'));
  slides[n].classList.add('active');
  createHearts(n);
}
function nextSlide(){
  if(currentSlide < slides.length-1) currentSlide++;
  showSlide(currentSlide);
}
function prevSlide(){
  if(currentSlide > 0) currentSlide--;
  showSlide(currentSlide);
}
showSlide(currentSlide);

/* Hearts Animation */
function createHearts(slideIndex){
  const heartsContainers = document.querySelectorAll('.hearts');
  heartsContainers.forEach(h => h.innerHTML=''); // reset
  const hearts = heartsContainers[slideIndex];
  if(!hearts) return;
  for(let i=0;i<15;i++){
    const heart = document.createElement('div');
    heart.innerHTML='❤️';
    heart.style.position='absolute';
    heart.style.left=Math.random()*100+'%';
    heart.style.animation=`fall ${2+Math.random()*3}s linear infinite`;
    hearts.appendChild(heart);
  }
}

/* Surprise Button */
const surpriseBtn = document.getElementById('surpriseBtn');
if(surpriseBtn){
  surpriseBtn.addEventListener('click',()=>{
    const audio = document.getElementById('valentineSong');
    if(audio) audio.play();
    alert('Surprise! 🎁💖');
  });
}
