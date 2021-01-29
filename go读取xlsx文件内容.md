# go读取excel表格数据



## 使用工具

`github.com/Luxurioust/excelize`
*百度到的都是使用这个 实际上已经改名了*
`github.com/360EntSecGroup-Skylar/excelize`


## 示例代码

```go
package agent

import (
	"fmt"
	"github.com/360EntSecGroup-Skylar/excelize"
)

func ImportFromXLS(file string) string {
	fmt.Println(file)
	f, err := excelize.OpenFile(file)
	if err != nil {
		fmt.Println(err)
		return err.Error()
	}

	// Get all the rows in the Sheet1.
	rows := f.GetRows("Sheet1")
	for _, row := range rows {
		for _, colCell := range row {
			fmt.Print(colCell, "\t")
		}
		fmt.Println()
	}

	return file
}

```

**结果**

```
序号	*所属大区	*地区	*职位	*姓名	性别	*手机号码	座机号	微信	邮箱	
1	华南	湖南长沙市宁乡县	县导	李四	男	XXXXXX	XXXXXX			
d:\a.xlsx

Process finished with exit code 0
```





## github地址

[360EntSecGroup-Skylar/excelize](https://github.com/360EntSecGroup-Skylar/excelize)