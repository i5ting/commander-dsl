commander-dsl
=============

https://github.com/tj/commander.js


## 原型

```
program
  .version(version)
	.usage(" badge -n badge-cli -f [md] -t [npm] ")
	.option('-n, --name [name]', 'npm name,for example: q')
  .option('-f, --format [format]', '可选值：url, markdown（默认值）, html, textile, rdoc, asciidoc, rst')
  .option('-t, --type [type]', '可选值：npm（默认值）, ruby    , python    , bower    , github    , nuget    , php    , cocoapods    , perl  ')
	.option('-v, --verbose', '打印详细日志')
  .parse(process.argv);
	
```

## cli-config.json

```
{
	name:'badge',
	desc:"a cli tools for badge",
	options:[
		{
			sname:'-t',
			lname:'--type',
			type:string,
			desc:"可选值：npm（默认值）, ruby    , python    , bower "
		}
	]
}
```

## call

```
var cli = require('commander-dsl');

cli.init({
	aaa:function(options){
	}
},'cli-config.json');
```



