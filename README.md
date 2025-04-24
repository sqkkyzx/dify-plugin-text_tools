# 文本处理插件

https://github.com/sqkkyzx/dify-plugin-text_tools

本插件提供了一系列用于文本处理的工具，涵盖了正则表达式提取、文本替换、哈希计算、编码解码以及 Deepseek 思维链清理等功能，满足不同的文本处理需求。

## 工具列表

### 1. 正则提取文本 (`text_regex_extract`)
- **功能**：使用正则表达式从文本中提取内容，支持在正则表达式中使用 `()` 捕获组提取结果。`text` 仅输出第一个匹配结果；`json` 输出所有匹配结果。
- **参数**：
  - `input_text`：输入文本，必填。
  - `regex_pattern`：正则表达式，必填。
  - `regex_ignorecase`：是否忽略大小写，默认 `false`。
  - `regex_multiline`：是否让 `^` 和 `$` 每行生效，默认 `false`。
  - `regex_dotall`：是否让 `.` 匹配包括换行在内的所有字符，默认 `false`。
  - `regex_ascii`：是否让 `\w`, `\d`, `\s` 只匹配 ASCII，默认 `false`。

### 2. 文本替换 (`text_replace`)
- **功能**：将字符串中的所有匹配项替换为目标字符串，支持使用正则表达式，支持在正则表达式中使用 `()` 捕获组进行查找和替换。
- **参数**：
  - `input_text`：输入文本，必填。
  - `search_text`：查找内容，必填，如果开启正则表达式，则此处作为正则表达式进行查找。
  - `replace_text`：替换文本，必填。
  - `use_regex`：是否使用正则表达式，默认 `false`。
  - `regex_ignorecase`：是否忽略大小写，默认 `false`。
  - `regex_multiline`：是否让 `^` 和 `$` 每行生效，默认 `false`。
  - `regex_dotall`：是否让 `.` 匹配包括换行在内的所有字符，默认 `false`。
  - `regex_ascii`：是否让 `\w`, `\d`, `\s` 只匹配 ASCII，默认 `false`。

### 3. 哈希计算 (`hash_calculator`)
- **功能**：使用 MD5、SHA256 或 SHA1 算法计算输入文本的哈希值。
- **参数**：
  - `input_text`：输入文本，必填。
  - `algorithm`：哈希算法，可选 `md5`、`sha256`、`sha1`，必填。

### 4. 编码解码 (`encode_decode`)
- **功能**：使用 URL、Base64 或 Unicode 进行文本的编码或解码。
- **参数**：
  - `input_text`：输入文本，必填。
  - `operation`：操作类型，可选 `url_encode`、`url_decode`、`base64_encode`、`base64_decode`、`unicode_encode`、`unicode_decode`，必填。

### 5. Deepseek 思维链清理 (`ds_thought_clean`)
- **功能**：清理 Deepseek 输出的思维链内容，生成简洁的回复。
- **参数**：
  - `provider`：模型提供商，目前仅支持 `deepseek`，必填。
  - `content`：上游 LLM 输出内容，必填。

## 使用说明

1. **安装插件**：将插件集添加到您的开发环境中。
2. **调用工具**：根据需求选择相应的工具，并传入必要的参数。
3. **获取结果**：工具将返回处理后的结果，您可以根据需要进行进一步的操作。


## 贡献者

- **作者**：yizixuan 

如果您有任何问题或建议，请随时联系开发者。


---

# TextTools Plugin For Dify

https://github.com/sqkkyzx/dify-plugin-text_tools

This plugin provides a series of tools for text processing, covering functions such as regular expression extraction, text replacement, hash calculation, encoding and decoding, as well as Deepseek thought chain cleaning, to meet different text processing needs.

## Tool list

### 1. Regular expression extraction of text (`text_regex_extract`)
- **Function**: Extract content from text using regular expressions, supporting the use of `()` capture groups in the regular expression to extract results. `text` only outputs the first matching result; `json` outputs all matching results.
- **Parameters**:
  - `input_text`: Input text, required.
  - `regex_pattern`: Regular expression, required.
  - `regex_ignorecase`: Whether to ignore case, default `false`.
  - `regex_multiline`: Whether to make `^` and `$` take effect on each line, default `false`.
  - `regex_dotall`: Whether to make `.` match all characters including line breaks, default `false`.
  - `regex_ascii`: Whether to make `\w`, `\d`, `\s` only match ASCII characters, default `false`.

### 2. Text replacement (`text_replace`)
- **Function**: Replace all matching items in a string with the target string, supporting the use of regular expressions, and supporting the use of `()` capture groups in the regular expression for searching and replacement.
- **Parameters**:
  - `input_text`: Input text, required.
  - `search_text`: Search content, required. If regular expression is enabled, this will be used as the regular expression for searching.
  - `replace_text`: Replacement text, required.
  - `use_regex`: Whether to use regular expression, default `false`.
  - `regex_ignorecase`: Whether to ignore case, default `false`.
  - `regex_multiline`: Whether to make `^` and `$` take effect on each line, default `false`.
  - `regex_dotall`: Whether to make `.` match all characters including line breaks, default `false`.
  - `regex_ascii`: Whether to make `\w`, `\d`, `\s` only match ASCII characters, default `false`.

### 3. Hash calculation (`hash_calculator`)
- **Function**: Calculate the hash value of the input text using MD5, SHA256, or SHA1 algorithm.
- **Parameters**:
  - `input_text`: Input text, required.
  - `algorithm`: Hash algorithm, optional `md5`, `sha256`, `sha1`, required.

### 4. Encoding and decoding (`encode_decode`)
- **Function**: Encode or decode text using URL, Base64, or Unicode.
- **Parameters**:
  - `input_text`: Input text, required.
  - `operation`: Operation type, optional `url_encode`, `url_decode`, `base64_encode`, `base64_decode`, `unicode_encode`, `unicode_decode`, required.

### 5. Deepseek thought chain cleaning (`ds_thought_clean`)
- **Function**: Clean up the thought chain content output by Deepseek and generate a concise reply.
- **Parameters**:
  - `provider`: Model provider, currently only supports `deepseek`, required.
  - `content`: Output content of the upstream LLM, required.

## Instructions for use

1. **Install the plugin**: Add the plugin set to your development environment.
2. **Call the tool**: Select the appropriate tool according to your needs and pass in the necessary parameters.
3. **Get the result**: The tool will return the processed result, and you can perform further operations as needed.


## Contributors

- **Author**: yizixuan 

If you have any questions or suggestions, please feel free to contact the developer.