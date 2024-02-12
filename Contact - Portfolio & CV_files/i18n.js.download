(function(){var __webpack_modules__=({124:(function(module,exports,__webpack_require__){var __WEBPACK_AMD_DEFINE_RESULT__;!function(){'use strict'
var re={not_string:/[^s]/,not_bool:/[^t]/,not_type:/[^T]/,not_primitive:/[^v]/,number:/[diefg]/,numeric_arg:/[bcdiefguxX]/,json:/[j]/,not_json:/[^j]/,text:/^[^\x25]+/,modulo:/^\x25{2}/,placeholder:/^\x25(?:([1-9]\d*)\$|\(([^)]+)\))?(\+)?(0|'[^$])?(-)?(\d+)?(?:\.(\d+))?([b-gijostTuvxX])/,key:/^([a-z_][a-z_\d]*)/i,key_access:/^\.([a-z_][a-z_\d]*)/i,index_access:/^\[(\d+)\]/,sign:/^[+-]/}
function sprintf(key){return sprintf_format(sprintf_parse(key),arguments)}
function vsprintf(fmt,argv){return sprintf.apply(null,[fmt].concat(argv||[]))}
function sprintf_format(parse_tree,argv){var cursor=1,tree_length=parse_tree.length,arg,output='',i,k,ph,pad,pad_character,pad_length,is_positive,sign
for(i=0;i<tree_length;i++){if(typeof parse_tree[i]==='string'){output+=parse_tree[i]}
else if(typeof parse_tree[i]==='object'){ph=parse_tree[i]
if(ph.keys){arg=argv[cursor]
for(k=0;k<ph.keys.length;k++){if(arg==undefined){throw new Error(sprintf('[sprintf] Cannot access property "%s" of undefined value "%s"',ph.keys[k],ph.keys[k-1]))}
arg=arg[ph.keys[k]]}}
else if(ph.param_no){arg=argv[ph.param_no]}
else{arg=argv[cursor++]}
if(re.not_type.test(ph.type)&&re.not_primitive.test(ph.type)&&arg instanceof Function){arg=arg()}
if(re.numeric_arg.test(ph.type)&&(typeof arg!=='number'&&isNaN(arg))){throw new TypeError(sprintf('[sprintf] expecting number but found %T',arg))}
if(re.number.test(ph.type)){is_positive=arg>=0}
switch(ph.type){case 'b':arg=parseInt(arg,10).toString(2)
break
case 'c':arg=String.fromCharCode(parseInt(arg,10))
break
case 'd':case 'i':arg=parseInt(arg,10)
break
case 'j':arg=JSON.stringify(arg,null,ph.width?parseInt(ph.width):0)
break
case 'e':arg=ph.precision?parseFloat(arg).toExponential(ph.precision):parseFloat(arg).toExponential()
break
case 'f':arg=ph.precision?parseFloat(arg).toFixed(ph.precision):parseFloat(arg)
break
case 'g':arg=ph.precision?String(Number(arg.toPrecision(ph.precision))):parseFloat(arg)
break
case 'o':arg=(parseInt(arg,10)>>>0).toString(8)
break
case 's':arg=String(arg)
arg=(ph.precision?arg.substring(0,ph.precision):arg)
break
case 't':arg=String(!!arg)
arg=(ph.precision?arg.substring(0,ph.precision):arg)
break
case 'T':arg=Object.prototype.toString.call(arg).slice(8,-1).toLowerCase()
arg=(ph.precision?arg.substring(0,ph.precision):arg)
break
case 'u':arg=parseInt(arg,10)>>>0
break
case 'v':arg=arg.valueOf()
arg=(ph.precision?arg.substring(0,ph.precision):arg)
break
case 'x':arg=(parseInt(arg,10)>>>0).toString(16)
break
case 'X':arg=(parseInt(arg,10)>>>0).toString(16).toUpperCase()
break}
if(re.json.test(ph.type)){output+=arg}
else{if(re.number.test(ph.type)&&(!is_positive||ph.sign)){sign=is_positive?'+':'-'
arg=arg.toString().replace(re.sign,'')}
else{sign=''}
pad_character=ph.pad_char?ph.pad_char==='0'?'0':ph.pad_char.charAt(1):' '
pad_length=ph.width-(sign+arg).length
pad=ph.width?(pad_length>0?pad_character.repeat(pad_length):''):''
output+=ph.align?sign+arg+pad:(pad_character==='0'?sign+pad+arg:pad+sign+arg)}}}
return output}
var sprintf_cache=Object.create(null)
function sprintf_parse(fmt){if(sprintf_cache[fmt]){return sprintf_cache[fmt]}
var _fmt=fmt,match,parse_tree=[],arg_names=0
while(_fmt){if((match=re.text.exec(_fmt))!==null){parse_tree.push(match[0])}
else if((match=re.modulo.exec(_fmt))!==null){parse_tree.push('%')}
else if((match=re.placeholder.exec(_fmt))!==null){if(match[2]){arg_names|=1
var field_list=[],replacement_field=match[2],field_match=[]
if((field_match=re.key.exec(replacement_field))!==null){field_list.push(field_match[1])
while((replacement_field=replacement_field.substring(field_match[0].length))!==''){if((field_match=re.key_access.exec(replacement_field))!==null){field_list.push(field_match[1])}
else if((field_match=re.index_access.exec(replacement_field))!==null){field_list.push(field_match[1])}
else{throw new SyntaxError('[sprintf] failed to parse named argument key')}}}
else{throw new SyntaxError('[sprintf] failed to parse named argument key')}
match[2]=field_list}
else{arg_names|=2}
if(arg_names===3){throw new Error('[sprintf] mixing positional and named placeholders is not (yet) supported')}
parse_tree.push({placeholder:match[0],param_no:match[1],keys:match[2],sign:match[3],pad_char:match[4],align:match[5],width:match[6],precision:match[7],type:match[8]})}
else{throw new SyntaxError('[sprintf] unexpected placeholder')}
_fmt=_fmt.substring(match[0].length)}
return sprintf_cache[fmt]=parse_tree}
if(true){exports.sprintf=sprintf
exports.vsprintf=vsprintf}
if(typeof window!=='undefined'){window['sprintf']=sprintf
window['vsprintf']=vsprintf
if(true){!(__WEBPACK_AMD_DEFINE_RESULT__=(function(){return{'sprintf':sprintf,'vsprintf':vsprintf}}).call(exports,__webpack_require__,exports,module),__WEBPACK_AMD_DEFINE_RESULT__!==undefined&&(module.exports=__WEBPACK_AMD_DEFINE_RESULT__))}}}();})});var __webpack_module_cache__={};function __webpack_require__(moduleId){var cachedModule=__webpack_module_cache__[moduleId];if(cachedModule!==undefined){return cachedModule.exports;}
var module=__webpack_module_cache__[moduleId]={exports:{}};__webpack_modules__[moduleId](module,module.exports,__webpack_require__);return module.exports;}
!function(){__webpack_require__.n=function(module){var getter=module&&module.__esModule?function(){return module['default'];}:function(){return module;};__webpack_require__.d(getter,{a:getter});return getter;};}();!function(){__webpack_require__.d=function(exports,definition){for(var key in definition){if(__webpack_require__.o(definition,key)&&!__webpack_require__.o(exports,key)){Object.defineProperty(exports,key,{enumerable:true,get:definition[key]});}}};}();!function(){__webpack_require__.o=function(obj,prop){return Object.prototype.hasOwnProperty.call(obj,prop);}}();!function(){__webpack_require__.r=function(exports){if(typeof Symbol!=='undefined'&&Symbol.toStringTag){Object.defineProperty(exports,Symbol.toStringTag,{value:'Module'});}
Object.defineProperty(exports,'__esModule',{value:true});};}();var __webpack_exports__={};!function(){"use strict";__webpack_require__.r(__webpack_exports__);__webpack_require__.d(__webpack_exports__,{__:function(){return __;},_n:function(){return _n;},_nx:function(){return _nx;},_x:function(){return _x;},createI18n:function(){return createI18n;},defaultI18n:function(){return default_i18n;},getLocaleData:function(){return getLocaleData;},hasTranslation:function(){return hasTranslation;},isRTL:function(){return isRTL;},resetLocaleData:function(){return resetLocaleData;},setLocaleData:function(){return setLocaleData;},sprintf:function(){return sprintf_sprintf;},subscribe:function(){return subscribe;}});;function memize(fn,options){var size=0;var head;var tail;options=options||{};function memoized(){var node=head,len=arguments.length,args,i;searchCache:while(node){if(node.args.length!==arguments.length){node=node.next;continue;}
for(i=0;i<len;i++){if(node.args[i]!==arguments[i]){node=node.next;continue searchCache;}}
if(node!==head){if(node===tail){tail=node.prev;}
(node.prev).next=node.next;if(node.next){node.next.prev=node.prev;}
node.next=head;node.prev=null;(head).prev=node;head=node;}
return node.val;}
args=new Array(len);for(i=0;i<len;i++){args[i]=arguments[i];}
node={args:args,val:fn.apply(null,args),};if(head){head.prev=node;node.next=head;}else{tail=node;}
if(size===(options).maxSize){tail=(tail).prev;(tail).next=null;}else{size++;}
head=node;return node.val;}
memoized.clear=function(){head=null;tail=null;size=0;};return memoized;}
var sprintf=__webpack_require__(124);var sprintf_default=__webpack_require__.n(sprintf);;const logErrorOnce=memize(console.error);function sprintf_sprintf(format,...args){try{return sprintf_default().sprintf(format,...args);}catch(error){if(error instanceof Error){logErrorOnce('sprintf error: \n\n'+error.toString());}
return format;}};var PRECEDENCE,OPENERS,TERMINATORS,PATTERN;PRECEDENCE={'(':9,'!':8,'*':7,'/':7,'%':7,'+':6,'-':6,'<':5,'<=':5,'>':5,'>=':5,'==':4,'!=':4,'&&':3,'||':2,'?':1,'?:':1,};OPENERS=['(','?'];TERMINATORS={')':['('],':':['?','?:'],};PATTERN=/<=|>=|==|!=|&&|\|\||\?:|\(|!|\*|\/|%|\+|-|<|>|\?|\)|:/;function postfix(expression){var terms=[],stack=[],match,operator,term,element;while((match=expression.match(PATTERN))){operator=match[0];term=expression.substr(0,match.index).trim();if(term){terms.push(term);}
while((element=stack.pop())){if(TERMINATORS[operator]){if(TERMINATORS[operator][0]===element){operator=TERMINATORS[operator][1]||operator;break;}}else if(OPENERS.indexOf(element)>=0||PRECEDENCE[element]<PRECEDENCE[operator]){stack.push(element);break;}
terms.push(element);}
if(!TERMINATORS[operator]){stack.push(operator);}
expression=expression.substr(match.index+operator.length);}
expression=expression.trim();if(expression){terms.push(expression);}
return terms.concat(stack.reverse());};var OPERATORS={'!':function(a){return!a;},'*':function(a,b){return a*b;},'/':function(a,b){return a/b;},'%':function(a,b){return a%b;},'+':function(a,b){return a+b;},'-':function(a,b){return a-b;},'<':function(a,b){return a<b;},'<=':function(a,b){return a<=b;},'>':function(a,b){return a>b;},'>=':function(a,b){return a>=b;},'==':function(a,b){return a===b;},'!=':function(a,b){return a!==b;},'&&':function(a,b){return a&&b;},'||':function(a,b){return a||b;},'?:':function(a,b,c){if(a){throw b;}
return c;},};function evaluate(postfix,variables){var stack=[],i,j,args,getOperatorResult,term,value;for(i=0;i<postfix.length;i++){term=postfix[i];getOperatorResult=OPERATORS[term];if(getOperatorResult){j=getOperatorResult.length;args=Array(j);while(j--){args[j]=stack.pop();}
try{value=getOperatorResult.apply(null,args);}catch(earlyReturn){return earlyReturn;}}else if(variables.hasOwnProperty(term)){value=variables[term];}else{value=+term;}
stack.push(value);}
return stack[0];};function compile(expression){var terms=postfix(expression);return function(variables){return evaluate(terms,variables);};};function pluralForms(expression){var evaluate=compile(expression);return function(n){return+evaluate({n:n});};};var DEFAULT_OPTIONS={contextDelimiter:'\u0004',onMissingKey:null,};function getPluralExpression(pf){var parts,i,part;parts=pf.split(';');for(i=0;i<parts.length;i++){part=parts[i].trim();if(part.indexOf('plural=')===0){return part.substr(7);}}}
function Tannin(data,options){var key;this.data=data;this.pluralForms={};this.options={};for(key in DEFAULT_OPTIONS){this.options[key]=options!==undefined&&key in options?options[key]:DEFAULT_OPTIONS[key];}}
Tannin.prototype.getPluralForm=function(domain,n){var getPluralForm=this.pluralForms[domain],config,plural,pf;if(!getPluralForm){config=this.data[domain][''];pf=(config['Plural-Forms']||config['plural-forms']||config.plural_forms);if(typeof pf!=='function'){plural=getPluralExpression(config['Plural-Forms']||config['plural-forms']||config.plural_forms);pf=pluralForms(plural);}
getPluralForm=this.pluralForms[domain]=pf;}
return getPluralForm(n);};Tannin.prototype.dcnpgettext=function(domain,context,singular,plural,n){var index,key,entry;if(n===undefined){index=0;}else{index=this.getPluralForm(domain,n);}
key=singular;if(context){key=context+this.options.contextDelimiter+singular;}
entry=this.data[domain][key];if(entry&&entry[index]){return entry[index];}
if(this.options.onMissingKey){this.options.onMissingKey(singular,domain);}
return index===0?singular:plural;};;const DEFAULT_LOCALE_DATA={'':{plural_forms(n){return n===1?0:1;}}};const I18N_HOOK_REGEXP=/^i18n\.(n?gettext|has_translation)(_|$)/;const createI18n=(initialData,initialDomain,hooks)=>{const tannin=new Tannin({});const listeners=new Set();const notifyListeners=()=>{listeners.forEach(listener=>listener());};const subscribe=callback=>{listeners.add(callback);return()=>listeners.delete(callback);};const getLocaleData=(domain='default')=>tannin.data[domain];const doSetLocaleData=(data,domain='default')=>{tannin.data[domain]={...tannin.data[domain],...data};tannin.data[domain]['']={...DEFAULT_LOCALE_DATA[''],...tannin.data[domain]?.['']};delete tannin.pluralForms[domain];};const setLocaleData=(data,domain)=>{doSetLocaleData(data,domain);notifyListeners();};const addLocaleData=(data,domain='default')=>{tannin.data[domain]={...tannin.data[domain],...data,'':{...DEFAULT_LOCALE_DATA[''],...tannin.data[domain]?.[''],...data?.['']}};delete tannin.pluralForms[domain];notifyListeners();};const resetLocaleData=(data,domain)=>{tannin.data={};tannin.pluralForms={};setLocaleData(data,domain);};const dcnpgettext=(domain='default',context,single,plural,number)=>{if(!tannin.data[domain]){doSetLocaleData(undefined,domain);}
return tannin.dcnpgettext(domain,context,single,plural,number);};const getFilterDomain=(domain='default')=>domain;const __=(text,domain)=>{let translation=dcnpgettext(domain,undefined,text);if(!hooks){return translation;}
translation=hooks.applyFilters('i18n.gettext',translation,text,domain);return(hooks.applyFilters('i18n.gettext_'+getFilterDomain(domain),translation,text,domain));};const _x=(text,context,domain)=>{let translation=dcnpgettext(domain,context,text);if(!hooks){return translation;}
translation=hooks.applyFilters('i18n.gettext_with_context',translation,text,context,domain);return(hooks.applyFilters('i18n.gettext_with_context_'+getFilterDomain(domain),translation,text,context,domain));};const _n=(single,plural,number,domain)=>{let translation=dcnpgettext(domain,undefined,single,plural,number);if(!hooks){return translation;}
translation=hooks.applyFilters('i18n.ngettext',translation,single,plural,number,domain);return(hooks.applyFilters('i18n.ngettext_'+getFilterDomain(domain),translation,single,plural,number,domain));};const _nx=(single,plural,number,context,domain)=>{let translation=dcnpgettext(domain,context,single,plural,number);if(!hooks){return translation;}
translation=hooks.applyFilters('i18n.ngettext_with_context',translation,single,plural,number,context,domain);return(hooks.applyFilters('i18n.ngettext_with_context_'+getFilterDomain(domain),translation,single,plural,number,context,domain));};const isRTL=()=>{return 'rtl'===_x('ltr','text direction');};const hasTranslation=(single,context,domain)=>{const key=context?context+'\u0004'+single:single;let result=!!tannin.data?.[domain!==null&&domain!==void 0?domain:'default']?.[key];if(hooks){result=hooks.applyFilters('i18n.has_translation',result,single,context,domain);result=hooks.applyFilters('i18n.has_translation_'+getFilterDomain(domain),result,single,context,domain);}
return result;};if(initialData){setLocaleData(initialData,initialDomain);}
if(hooks){const onHookAddedOrRemoved=hookName=>{if(I18N_HOOK_REGEXP.test(hookName)){notifyListeners();}};hooks.addAction('hookAdded','core/i18n',onHookAddedOrRemoved);hooks.addAction('hookRemoved','core/i18n',onHookAddedOrRemoved);}
return{getLocaleData,setLocaleData,addLocaleData,resetLocaleData,subscribe,__,_x,_n,_nx,isRTL,hasTranslation};};;var external_wp_hooks_namespaceObject=window["wp"]["hooks"];;const i18n=createI18n(undefined,undefined,external_wp_hooks_namespaceObject.defaultHooks);var default_i18n=(i18n);const getLocaleData=i18n.getLocaleData.bind(i18n);const setLocaleData=i18n.setLocaleData.bind(i18n);const resetLocaleData=i18n.resetLocaleData.bind(i18n);const subscribe=i18n.subscribe.bind(i18n);const __=i18n.__.bind(i18n);const _x=i18n._x.bind(i18n);const _n=i18n._n.bind(i18n);const _nx=i18n._nx.bind(i18n);const isRTL=i18n.isRTL.bind(i18n);const hasTranslation=i18n.hasTranslation.bind(i18n);;}();(window.wp=window.wp||{}).i18n=__webpack_exports__;})();