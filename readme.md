### Clone Neovim Repository
Clone the Neovim repository from GitHub into your home directory (or any other directory where you have write permissions):

```bash
git clone https://github.com/neovim/neovim.git ~/neovim
```

### Build Neovim Locally
Navigate into the neovim directory:
```bash
cd ~/neovim
```
### Configure the build for a local installation:
This command tells Neovim's build system to install to ~/neovim.
```bash
make CMAKE_BUILD_TYPE=RelWithDebInfo CMAKE_INSTALL_PREFIX=$HOME/neovim
```

### Build Neovim:

```bash
make -j4
```
The -j4 flag specifies the number of parallel jobs to run during compilation. You can adjust this number according to the number of cores your CPU has (e.g., -j8 for 8 cores).

### Install Neovim Locally
Once the build process completes, install Neovim locally:
```bash
make install
```
### Add Neovim to PATH
This makes it easier to run Neovim from anywhere in the terminal, you can add its bin directory to your PATH:
Add the following line to your ~/.bashrc, ~/.bash_profile, or ~/.zshrc file:

```bash
export PATH=$HOME/neovim/bin:$PATH
```
Then, apply the changes:
```bash
exec zsh # or bash etc
```
Or (Use exec or source)
```bash
source ~/.bashrc  # or ~/.bash_profile or ~/.zshrc depending on your shell
```

### Verify Installation
You can now verify that Neovim is installed and accessible:

```bash
nvim --version
```
This command should display the Neovim version, confirming that the installation was successful.
Notes

Then install AstroNvim
```bash
git clone --depth 1 https://github.com/AstroNvim/AstroNvim ~/.config/nvim
```
Now install AstroNvim plugins with the nvim command
```bash
nvim
```
