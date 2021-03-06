# xkcli

Simple terminal based xkcd comic viewer. CLI will display the title, alt text, and image of a comic.

## Usage

Installation: `npm i -g xkcli` or `yarn global add xkcli`

NOTE: The first command run should be `xk c`. This command not only fetches the latest comic, but saves the comic number as well. Other options, such as `xk s <value>` and `xk r` are reliant on the latest comic number (see descriptions below).

```bash
Usage: xk [commands] [options]

Options:
  -v, --version               output the version number
  -h, --help                  output usage information

Commands:
  c                           display the latest comic
  p                           display the previous comic based on the present comic
  n                           display the next comic based on the present comic
  s <value>                   display a specific comic ranging from the first to latest
  r                           display random comic ranging from the first to latest
  o [options] <chalkOptions>  configure chalk options to change color of output text 
  d,                          display filepath to data storage location
```



## Comic

These subcommands allows for the fetching and displaying the comics. 


__Examples:__

* current, next, previous, and random subcommands have similar invocations:

  ```bash
  xk c
  xk n
  xk p
  xk r
  ```

* specific comic

  ```bash
  xk s 123
  ```



## Style

This subcommand allows for the stylistic manipulation of the title and alt text. These texts can be stylized using the available [**chalk**](https://github.com/chalk/chalk#styles) options.


__Examples:__

* style the title text (text above image) with __title__ option (`-t` or `--title`)

  ```bash
  xk o -t bold.whiteBright.bgYellowBright
  ```

* style the alt text (text below image) with the __alt__ option (`-a` or `--alt`)

  ```bash
  xk o -a bold.whiteBright.bgYellowBright
  ```

* style both texts at once with the __both__ option (`-b` or `--both`)

  ```bash
  xk o -b bold.whiteBright.bgYellowBright,italic.greenBright.bgWhite
  ```

* locate data store location

  ```
  xk d
  ```

The value before the comma, `bold.whiteBright.bgBlackBright`, is applied to the title text, and value following the comma, `italic.yellowBright`, is applied to the alt text.


## Contributions
Contributions are welcome. 


## References
[xkcd.com](https://xkcd.com/) | [xkcd api](https://xkcd.com/json.html)
