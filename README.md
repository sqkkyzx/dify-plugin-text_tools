# TextTools Plugin For Dify

**Author:** yizixuan
**Version:** 0.0.3
**Type:** tool

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

### 6. Word Count (`word_count`)
- **Function**: Count the number of lines, non-empty lines, characters, visible characters, Chinese characters, English words, English characters and characters excluding punctuation in the input text.
- **Parameters**:
  - `text`: The text to be counted, required.

## Instructions for use

1. **Install the plugin**: Add the plugin set to your development environment.
2. **Call the tool**: Select the appropriate tool according to your needs and pass in the necessary parameters.
3. **Get the result**: The tool will return the processed result, and you can perform further operations as needed.

If you have any questions or suggestions, please feel free to contact the developer.