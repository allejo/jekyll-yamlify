<!--
When using this README template, replace the following:
  - `USERNAME/REPO` with the username + repo name
  - `liquid_snippet.html` with the name of your snippet
-->

# Jekyll Pure Liquid `PROJECT_NAME`

[![Unit Tests](https://github.com/USERNAME/REPO/workflows/Unit%20Tests/badge.svg)](/actions?query=workflow%3A%22Unit+Tests%22)
[![Latest release](https://img.shields.io/github/release/USERNAME/REPO.svg)](/releases/latest)
[![ko-fi](https://img.shields.io/static/v1.svg?label=&message=Support%20me%20on%20Ko-fi&color=333&logo=ko-fi)](https://ko-fi.com/Q5Q4J7IX)
[![Buy me a coffee](https://img.shields.io/static/v1.svg?label=&message=Buy%20me%20a%20coffee&color=333&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/allejo)

## Usage

Alright, so how do you use it?

1. Download the `liquid_snippet.html` file from [the latest release](/releases/latest) or [the master branch](_includes/liquid_snippet.html)
2. Toss that file in your `_includes` folder
3. Where you typically would put `{{ content }}` in your layout, you would instead use this Liquid tag to output your page's content:

   ```liquid
   {% include liquid_snippet.html arg1=site.whatever %}
   ```

## Parameters

This snippet is highly customizable. Here are the available parameters to change the behavior of the snippet.

| Parameter       |  Type  | Default | Description |
| --------------  | :----: | :-----: | ----------- |

## Performance

The performance impact of this snippet on your site is pretty negligible. The stats below were gotten from Jekyll's `--profile` option.

```
Filename                                         | Count |    Bytes |  Time
-------------------------------------------------+-------+----------+------

```

## License

This snippet may be redistributed under the [MIT](LICENSE.md) license.
