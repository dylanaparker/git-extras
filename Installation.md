## Debian

```bash
$ sudo apt-get update
$ sudo apt-get install git-extras
```

## Mac

```bash
$ brew install git-extras
```

## Clone / Tarball:

```bash
$ git clone https://github.com/tj/git-extras.git
$ cd git-extras
# checkout the latest tag
$ git checkout $(git describe --tags $(git rev-list --tags --max-count=1))
$ [sudo] make install
```

One-liner:

```bash
curl -sSL http://git.io/git-extras-setup | sudo bash /dev/stdin
```

## Windows (use it at your own risk)

First, please install `Git for Windows 2.x` from 'https://github.com/git-for-windows/git/releases'
and the basic [msys2][1].
Second, clone the `git-extras` repo into any folder you like.
```bash
git clone https://github.com/tj/git-extras.git
# checkout the latest tag (optional)
git checkout $(git describe --tags $(git rev-list --tags --max-count=1))
```

After that, execute the `install.cmd` in the command prompt, with the path your `Git for Windows 2.x` is installed.
For example, I install it in the folder called `C:\SCM\PortableGit` and
the `PREFIX` should be `C:\SCM\PortableGit\mingw64` (for 64-bit release)
or `C:\SCM\PortableGit\mingw32` (for 32-bit release). So I will execute the `install.cmd` like this:
```batch
install.cmd "C:\SCM\PortableGit\mingw64"
```

Last, please copy `colrm.exe` and `column.exe` from `folder-your-msys2-installed/usr/bin` to
`folder-your-git-installed/usr/bin`.
Enjoy `git-extras`!

[1]: http://sourceforge.net/projects/msys2/
