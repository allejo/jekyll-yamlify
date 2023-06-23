# Jekyll Pure Liquid YAMLify

[![Unit Tests](https://github.com/allejo/jekyll-yamlify/workflows/Unit%20Tests/badge.svg)](/actions?query=workflow%3A%22Unit+Tests%22)
[![Latest release](https://img.shields.io/github/release/allejo/jekyll-yamlify.svg)](/releases/latest)
[![ko-fi](https://img.shields.io/static/v1.svg?label=&message=Support%20me%20on%20Ko-fi&color=333&logo=ko-fi)](https://ko-fi.com/Q5Q4J7IX)
[![Buy me a coffee](https://img.shields.io/static/v1.svg?label=&message=Buy%20me%20a%20coffee&color=333&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/allejo)

GitHub Pages can't run Jekyll plug-ins and Jekyll, nor Liquid, have built-in filters to pretty print YAML. For theme authors, if you want to share any YAML from your `_config.yaml`, to document theme settings, you are stuck with having to copy/paste the YAML. These changes do not stay in sync with your `_config.yml` for obvious reasons if you're copy and pasting.

As part of my Pure Liquid project, I wrote this solution entirely in Liquid to pretty print YAML via an `{% include %}` snippet.

## Usage

Alright, so how do you use it?

1. Download the `yamlify.html` file from [the latest release](/releases/latest) or [the main branch](_includes/yamlify.html)
2. Toss that file in your `_includes` folder
3. Now, whenever you want to pretty print an object as YAML, you can use this include like so,

   ```liquid
   {% include yamlify.html key="yaml_demo" value=site.yaml_demo %}
   ```

   and this will output something along the lines of,

   ```yaml
   yaml_demo:
     my-string: "Hello world"
     my-boolean: true
     my-date: "2020-03-14"
     my-number: 12345
     my-str-array:
       - "apple"
       - "orange"
       - "pear"
     my-colors:
       red: "#f00"
       green: "#0f0"
       blue: "#00f"
   ```

## Parameters

This snippet is highly customizable. Here are the available parameters to change the behavior of the snippet.

| Parameter       |  Type  | Default | Description |
| --------------  | :----: | :-----: | ----------- |
| `value`         | any    | <sup>*</sup> | any YAML-compatible value that will be written out as prettified YAML |
| `key`           | string | ''      | a top-level YAML key to use when printing out the given value |
| `include_path`  | string | 'yamilfy.html' | the relative path to this include; use this is you rename the include or put it subfolders |
| `indent_chars`  | string | '  '    | the indentation that will be used for each line |
| `indent_count`  | int    | 1       | the amount of times a given value needs to be indented when written |

<sup>*</sup> This is a required parameter

## Performance

The performance impact of this snippet on your site is pretty negligible. The stats below were gotten from Jekyll's `--profile` option.

```
Filename                                         | Count |    Bytes |  Time
-------------------------------------------------+-------+----------+------

```

## License

This snippet may be redistributed under the [MIT](LICENSE.md) license.
