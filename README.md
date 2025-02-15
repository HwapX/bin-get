# bin-get

![Tests](https://github.com/HwapX/bin-get/actions/workflows/tests.yml/badge.svg)

Get binaries from Github Releases in a convenient way!

Why [Deno](https://deno.land)?

- Only dependency for `bin-get.ts` would be `deno` itself (To install `curl -fsSL https://deno.land/install.sh | sudo DENO_INSTALL=/usr/local sh`)
- Better error management
- Use the power of TypeScript!
- By default no filesystem, network or environment access
- Look at that cute Deno logo!

## Usage

Install package in `/usr/bin` without explicitly installing `bin-get.ts`

```bash
sudo $(which deno) run --allow-all https://raw.githubusercontent.com/HwapX/bin-get/main/bin-get.ts install helm/helm
```

Install package in a user accessible location:

```bash
deno run --allow-all https://raw.githubusercontent.com/HwapX/bin-get/main/bin-get.ts install helm/helm --directory ~/.bin

```

Or install `bin-get`

```bash
deno install --allow-all https://raw.githubusercontent.com/HwapX/bin-get/main/bin-get.ts
```

## Contributing

Use [Github Codespaces](https://github.com/features/codespaces)/[vscode devcontainers](https://code.visualstudio.com/docs/remote/containers) if you want (development setup is already configured!)

- Add test if necessary
- Makes sure tests pass before creating a pull request
- Have fun! :-)

## Related projects

- [deb-get](https://github.com/wimpysworld/deb-get): *deb-get makes it easy to install and update .debs published in 3rd party apt repositories or made available via direct download on websites or GitHub release pages.*

## Todo

- Add code to verify binaries with checksum
- Add more tests with different packages
