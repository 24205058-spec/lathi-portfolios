// Generate particles
const container = document.getElementById('particles');
const colors = ['#a78bfa','#ec4899','#38bdf8','#f9a8d4','#ffffff'];
for(let i=0;i<60;i++){
  const p = document.createElement('div');
  p.classList.add('p');
  const size = Math.random()*4+2;
  p.style.cssText = `
    width:${size}px;height:${size}px;
    background:${colors[Math.floor(Math.random()*colors.length)]};
    left:${Math.random()*1080}px;
    bottom:-20px;
    opacity:${Math.random()*.6+.2};
    animation-duration:${Math.random()*15+10}s;
    animation-delay:${Math.random()*15}s;
    filter:blur(${Math.random()>0.7?'1px':'0px'});
  `;
  container.appendChild(p);
}
