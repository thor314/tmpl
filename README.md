# Templates
My "batteries-and-more-included" templates with `cargo-generate`.

## Why bother with templates? 
- Sanity testing is great. Templates like this make it easy to try out new libraries and test features. 
- Save time setting up tools. Tools are great. I want them available with minimal fiddling.
- How do I use `$TOOL` again? Templates remind me how to use my tools, even when I haven't picked them up recently.

## Current Features:
- CI on pull-requests: checks and tests 
- CI with dependabot to update dependencies. Note that, since the template repo inserts symbols Cargo can't parse, this feature keeps dependencies in generated libraries up to date, but not in the template repo itself.
- Automerge dependabot pull requests (this is insecure, but convenient as heck, and see above note.)
- 4 options for sync/async, bin/lib templates
- A template `clap` CLI tools
- Logging with `log` and `env_logger`
- Error handling with `anyhow` and `this-error`
- Environment variables with `dotenv`
- Input validation with `validator`
- Benching with `criterion` and `iai`
- Test fixtures with `rstest`
- Property testing (fuzzing) with `quickcheck` and `arbitrary`
- Opinionated formatting preferences in `rustfmt.toml`
- Sensible default `.gitignore` settings
- Licensing: permissive dual Unlicense/MIT licensing
- Several optional common dependencies; won't be built unless used

## To do:
More templates:
- Macro, Procedural Macro examples
- Rocket HTTP server template
- TUI template, similar to: https://github.com/orhun/rust-tui-template
- Rhai-script examples

## Usage
```sh
cargo install cargo-generate
# defaults to --bin over --lib
cargo generate thor314/tmpl [--lib] [--async={false|true}]  [-n YOUR_REPO_NAME] 
# managing fmt in a template repo sucks, do it yourself
cd YOUR_REPO_NAME && cargo fmt
```

## Overkill?
Yes. But I'd rather have the overkill all-the-features as a reference than to not have them. Save time, do it once is
the MO.

## Know a cool tool I don't?
Cool, drop an issue or a pull request!

## Alternatives:
- [rust-github/template](https://github.com/rust-github/template) - a lighter template for `cargo-generate`, with APACHE-MIT dual licensing
- fork this repo, modify it to your needs, and do it yourself, and maybe submit a pull? (**recommended**)
