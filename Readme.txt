
function rot13(str) { // LBH QVQ VG!
  var chrarr=[]; var chrcode=0; chrnew=""; var newstr="";
  for(var i=0; i<str.length; i++){
    chrcode = str.charCodeAt(i);
    //console.log(chrcode);
    if (str[i].match(/[a-zA-Z]/i)) {
      // alphabet letters found
      if((chrcode-13)<65){
      		var rem = 13-(chrcode-65);
			chrcode = 91 - rem;
      }
      else chrcode-=13;
    }
	//console.log(chrcode);    
   chrnew = String.fromCharCode(chrcode);
    //chrarr.push(chrcode);
    newstr+=chrnew;
  }
  //var newstr = String.fromCharCode(chrarr);
  console.log(newstr);
  console.log("=====End=====");
  return newstr;
}

// Change the inputs below to test
rot13("SERR PBQR PNZC");
