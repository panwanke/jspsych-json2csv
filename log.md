
```
根据以下函数写一个 html，使得可以添加或者拖入 json，导出 csv。

function JSON2CSV(objArray) {
	  const array = typeof objArray != "object" ? JSON.parse(objArray) : objArray;
	  let line = "";
	  let result = "";
	  const columns = [];
	  for (const row of array) {
	    for (const key in row) {
	      let keyString = key + "";
	      keyString = '"' + keyString.replace(/"/g, '""') + '",';
	      if (!columns.includes(key)) {
	        columns.push(key);
	        line += keyString;
	      }
	    }
	  }
	  line = line.slice(0, -1);
	  result += line + "\r\n";
	  for (const row of array) {
	    line = "";
	    for (const col of columns) {
	      let value = typeof row[col] === "undefined" ? "" : row[col];
	      if (typeof value == "object") {
	        value = JSON.stringify(value);
	      }
	      const valueString = value + "";
	      line += '"' + valueString.replace(/"/g, '""') + '",';
	    }
	    line = line.slice(0, -1);
	    result += line + "\r\n";
	  }
	  return result;
	}
```

需要优化的地方：
1. 可以拖入和选择多个文件夹，显示框显示文件夹名称。
2. 导出 csv 文件，与 json 文件同名, 路径相同。
3. 合并 转换csv 和下载 按钮

