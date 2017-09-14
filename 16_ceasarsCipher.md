function rot13(str) {

var newStr = str.split('').map(cipher).join('');
return newStr;
}
function cipher(letter) {
    var symbolregex = /[^a-zA-Z]/g;
      if(symbolregex.test(letter)) {
        return letter;
      }
      var codeAskii = letter.charCodeAt(0);
      if(codeAskii > 77) {
        codeAskii -= 13;
      } else {
        codeAskii += 13;
      }
    return  String.fromCharCode(codeAskii);
 }


console.log(
  rot13("SERR PBQR PNZC")
);
