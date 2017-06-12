# js-getStyleObject

function getStyleObject(a,b=null){//elem,pseudo
 const o={};
 for(let s,p=/\-([a-z])/g,m=window.getComputedStyle(a,b),l=m.length,i=0;i<l;++i){s=m[i];o[s.replace(p,function(a,b){return b.toUpperCase()})]=m.getPropertyValue(s)};
 return o;
}

//console.dir(getStyleObject(document.body))
