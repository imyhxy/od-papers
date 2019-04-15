```JavaScript
function GithubId(val) {
	return val.toLowerCase().replace(/ /g,'-')
		// single chars that are removed
		.replace(/[`~!@#$%^&*()+=<>?,./:;"'|{}\[\]\\–—]/g, '')
		// CJK punctuations that are removed
		.replace(/[　。？！，、；：“”【】（）〔〕［］﹃﹄“”‘’﹁﹂—…－～《》〈〉「」]/g, '')
}
```
