# Give yourself some Christmas magic with this script

#### 🔴 Disclaimer! Do not use it, it is not working correctly due to the issues of one package. I am going to fix it in the upcoming days. 🔴

A CLI tool which generates commit messages from your staged changes, 
which was built in Rust and using [OpenAI's Codex](https://openai.com/blog/openai-codex/).

## Installation

You can install `aa` by running the following command in your terminal.

```
curl -fsSL https://raw.githubusercontent.com/rookasrudzianskas/commit-open-ai/main/install.sh | sh -
```

Or, if you're an arch user, you can download it from the [AUR](https://aur.archlinux.org/) using

```sh
yay -S auto-commit
```

You may need to close and reopen your terminal after installation. Alternatively, you can download the binary corresponding to your OS from the [latest release](https://github.com/rookasrudzianskas/commit-open-ai).

## Usage

`aa` uses [OpenAI's Codex](https://openai.com/blog/openai-codex/), which is currently in public beta. 
First, if you want to use it, you will first need to to [request access to Codex](http://beta.openai.com/codex-waitlist). 
Once you get access, grab an API key from [your dashboard](https://beta.openai.com/), and save it to `OPENAI_API_KEY` as follows 
(you can also save it in your bash/zsh profile for persistence between sessions).

```bash
export OPENAI_API_KEY='sk-XXXXXXXX'
```

Once you have configured your environment, stage some changes by running, for example, `git add .`, and then run `aa`.

Of course, `aa` also includes some options, for editing the message before committing, or just printing the message to the terminal.

```sh
$ aa --help
Magically generate your commit messages.
Usage: auto-commit [OPTIONS]
Options:
  -v, --verbose...  More output per occurrence
  -q, --quiet...    Less output per occurrence
      --dry-run     Output the generated message, but don't create a commit.
  -r, --review      Edit the generated commit message before committing.
  -h, --help        Print help information
  -V, --version     Print version information
```
## Develop
Make sure you have the latest version of rust installed (use [rustup](https://rustup.rs/)). 
Then, you can build the project by running `cargo build`, and run it with `cargo run`.

## License
This project does not have complicated licenses, you can use it in any way you want :)
