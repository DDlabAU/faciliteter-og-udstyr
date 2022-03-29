---
theme: jekyll-theme-minimal
title: "Audiodesign"
permalink: /audiodesign/
---
<a name="top"></a>

# Audiodesign Faciliteter og Udstyr

## Indhold

<section id="tabelsetup"></section>

<script type="text/javascript">
var txtFile = new XMLHttpRequest();
txtFile.onload = function() {
    allText = txtFile.responseText;
    allTextLines = allText.split(/\r\n|\n/);
    var overskrift = "overskrift";
    for(var i = 1; i < allTextLines.length-1; i++) {
      elements = allTextLines[i].split(";");
      if (elements[0] === overskrift){
        document.getElementById("tabelsetup").innerHTML += '<a href="#' + i + '">' + elements[1] + '</a><br/>';
      }
    }
    document.getElementById("tabelsetup").innerHTML += '<br/><hr>';

    for(var i = 1; i < allTextLines.length-1; i++) {
        elements = allTextLines[i].split(";");
        if (elements[0] === overskrift){
          document.getElementById("tabelsetup").innerHTML += '<br/><h1 id=' + i + '><u>' + elements[1] + '</u></h1>';
        } else {
          document.getElementById("tabelsetup").innerHTML += '<h3>' + elements[0] + '</h3>';
          if(elements[1].includes("http")){
            document.getElementById("tabelsetup").innerHTML += '<br/><table><tr><td width="50%">' + '<img src="' + elements[1] + '" alt="' + elements[0] + '"' + 'style="width: 200px;" /></td> <td width="50%"><p>' + elements[2] + '<br/><b>' + elements[3]; + '</b></p></td></tr></table><br/>';
          } else if (elements[1] != "") {
            document.getElementById("tabelsetup").innerHTML += '<br/><table><tr><td width="50%">' + '<img src="images/' + elements[1] + '" alt="' + elements[0] + '"' + 'style="width: 200px;" /></td> <td width="50%"><p>' + elements[2] + '<br/><b>' + elements[3]; + '</b></p></td></tr></table><br/>';
          } else {
            document.getElementById("tabelsetup").innerHTML += '<br/><table><tr><td width="50%"></td><td width="50%"><p>' + elements[2] + '<br/><b>' + elements[3]; + '</b></p></td></tr></table><br/>';
          }
        }
    }
}

txtFile.open("get", "AudiodesignTabel.csv", true);
txtFile.send();
</script>

<a href="#top">Gå til toppen</a>
