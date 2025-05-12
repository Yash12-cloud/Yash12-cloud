
<img align="centre" width="400" src="https://static.wixstatic.com/media/b313a9_89ebec0c5f384c65a9551f0c1ec18ca9~mv2.gif" alt="">
💫 About Me:
🛠 I'm currently working on:<br>Building strong fundamentals in Java, C++, and Data Structures & Algorithms.<br><br>🤝 I'm looking to collaborate on:<br>DSA practice groups, coding challenges, and beginner-friendly dev projects.<br><br>🌱 I'm currently learning:<br>Java, C++, and DSA through problem practice .<br><br>💬 Ask me about:<br>Learning strategies, staying consistent with coding, or how to get started with DSA.<br><br>⚡ Fun fact:<br>I enjoy explaining coding concepts to others — it helps me understand better too!

#🚀 Languages and Tools I Use
<p><a target="_blank" href="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" style="display: inline-block;"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="c" width="42" height="42" /></a>
<a target="_blank" href="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" style="display: inline-block;"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="cplusplus" width="42" height="42" /></a>
<a target="_blank" href="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" style="display: inline-block;"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="java" width="42" height="42" /></a>
<a target="_blank" href="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" style="display: inline-block;"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="42" height="42" /></a></p>

#<🌐 Socials:
[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/yashnimje__) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/yash-nimje-838934342) [![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:yashnimje2005@gmail.com) 
<br>
#💻 Tech Stack:
![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white) ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
<br>
#📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=Yash12-cloud&theme=dark&hide_border=false&include_all_commits=false&count_private=false)<br/>
![](https://nirzak-streak-stats.vercel.app/?user=Yash12-cloud&theme=dark&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=Yash12-cloud&theme=dark&hide_border=false&include_all_commits=false&count_private=false&layout=compact)
<br>
#✍️ Random Dev Quote
![](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical)
<br>
🔝 Top Contributed Repo
![](https://github-contributor-stats.vercel.app/api?username=Yash12-cloud&limit=5&theme=dark&combine_all_yearly_contributions=true)

---
[![](https://visitcount.itsvg.in/api?id=Yash12-cloud&icon=0&color=0)](https://visitcount.itsvg.in)
import { animate, utils, createDraggable, createSpring } from 'animejs';

const [ $logo ] = utils.$('.logo.js');
const [ $button ] = utils.$('button');
let rotations = 0;

// Created a bounce animation loop
animate('.logo.js', {
  scale: [
    { to: 1.25, ease: 'inOut(3)', duration: 200 },
    { to: 1, ease: createSpring({ stiffness: 300 }) }
  ],
  loop: true,
  loopDelay: 250,
});

// Make the logo draggable around its center
createDraggable('.logo.js', {
  container: [0, 0, 0, 0],
  releaseEase: createSpring({ stiffness: 200 })
});

// Animate logo rotation on click
const rotateLogo = () => {
  rotations++;
  $button.innerText = `rotations: ${rotations}`;
  animate($logo, {
    rotate: rotations * 360,
    ease: 'out(4)',
    duration: 1500,
  });
}

$button.addEventListener('click', rotateLogo);
