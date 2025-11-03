
<h1 align="center">Hey there 👋 I´m Radek</h1>

###

<div align="center">
  <img height="150" src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif"  />
</div>

###


<h3 align="center">🔥   my slogan :  the error is always in front of the monitor</h3>

###
<h3 align="left">👩‍💻  About Me</h3>

###

<p align="left">I'm... from ....Germany<br><br>-- 📚 I'm currently learning ...JavaScript<br><br>-- finished with studies expected August 2026<br><br>--my progress : watch and enjoy my repos from time to time</p>

###

<h3 align="left">🛠 Language and tools</h3>


###

<div align="left">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="40" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="40" alt="css logo"  />
  <img width="12" />
  <a href ="https://code.visualstudio.com/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" height="40" alt="vscode logo"  /></a>
  <img width="12" />
  <a href = "https://github.com/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" height="40" alt="github logo"  /></a>
  <img width="12" />
  <a href = "https://filezilla-project.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/filezilla/filezilla-plain.svg" height="40" alt="filezilla logo"  /></a>
  <img width="12" />
  <a href = "https://filezilla-project.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/chrome/chrome-original.svg" height="40" alt="chrome logo"  /></a>
 <a href = "https://discord.com/"> <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/discord/default.svg" width="52" height="40" alt="discord logo"  /></a>


</div>

<?php
session_start();
$counter_name = "counter.txt";

// Check if a text file exists. If not create one and initialize it to zero.
if (!file_exists($counter_name)) {
  $f = fopen($counter_name, "w");
  fwrite($f,"0");
  fclose($f);
}

// Read the current value of our counter file
$f = fopen($counter_name,"r");
$counterVal = fread($f, filesize($counter_name));
fclose($f);

// Has visitor been counted in this session?
// If not, increase counter value by one
if(!isset($_SESSION['hasVisited'])){
  $_SESSION['hasVisited']="yes";
  $counterVal++;
  $f = fopen($counter_name, "w");
  fwrite($f, $counterVal);
  fclose($f); 
}

$counterVal = str_pad($counterVal, 5, "0", STR_PAD_LEFT);
$chars = preg_split('//', $counterVal);

$im = imagecreatefrompng("canvas.png");
$src1 = imagecreatefrompng("$chars[1].png");
$src2 = imagecreatefrompng("$chars[2].png");
$src3 = imagecreatefrompng("$chars[3].png");
$src4 = imagecreatefrompng("$chars[4].png");
$src5 = imagecreatefrompng("$chars[5].png");

imagecopymerge($im, $src1, 0, 0, 0, 0, 56, 75, 100);
imagecopymerge($im, $src2, 60, 0, 0, 0, 56, 75, 100);
imagecopymerge($im, $src3, 120, 0, 0, 0, 56, 75, 100);
imagecopymerge($im, $src4, 180, 0, 0, 0, 56, 75, 100);
imagecopymerge($im, $src5, 240, 0, 0, 0, 56, 75, 100);

// Output and free from memory
header('Content-Type: image/png');
echo imagepng($im);
imagedestroy($im);
?>


###

<p align="left"></p>
