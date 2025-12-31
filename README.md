# Alink教程中的预测例子 Prediction Examples in the Alink Tutorial

Alink教程中的两个预测例子：输入年份，预测GMV；输入一段评论，分析其情感色彩（褒义贬义/正向负向）。
Two prediction examples in the Alink tutorial: input a year to predict GMV; input a piece of feedback to analyze its sentiment (positive/negative).## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| pred_gmv | Alink教程第1章5.4节的Pipeline预测。输入年份，预测GMV。 |
| calc | Alink教程第23章4节的情感预测。输入一段评论，分析其情感色彩（褒义贬义/正向负向）。 |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1804079084099594](https://mcp.xiaobenyang.com/inspector/1804079084099594)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1804079084099594](https://mcp.xiaobenyang.com/inspector/1804079084099594)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "Alink教程中的预测例子": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1804079084099594/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "Alink教程中的预测例子": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1804079084099594/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "Alink教程中的预测例子": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1804079084099594",
          },
          "transport": "stdio"
        }
      }
}

```
