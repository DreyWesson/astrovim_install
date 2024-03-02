Clone Neovim Repository

Next, clone the Neovim repository from GitHub into your home directory (or any other directory where you have write permissions):

bash

git clone https://github.com/neovim/neovim.git ~/neovim

3. Build Neovim Locally

Navigate into the neovim directory:

bash

cd ~/neovim

Configure the build for a local installation:

bash

make CMAKE_BUILD_TYPE=RelWithDebInfo CMAKE_INSTALL_PREFIX=$HOME/neovim

This command tells Neovim's build system to install to ~/neovim.

Now, build Neovim:

bash

make -j4

The -j4 flag specifies the number of parallel jobs to run during compilation. You can adjust this number according to the number of cores your CPU has (e.g., -j8 for 8 cores).
4. Install Neovim Locally

Once the build process completes, install Neovim locally:

bash

make install

5. Add Neovim to PATH (Optional)

To make it easier to run Neovim from anywhere in the terminal, you can add its bin directory to your PATH:

Add the following line to your ~/.bashrc, ~/.bash_profile, or ~/.zshrc file:

bash

export PATH=$HOME/neovim/bin:$PATH

Then, apply the changes:

bash

source ~/.bashrc  # or ~/.bash_profile or ~/.zshrc depending on your shell

6. Verify Installation

You can now verify that Neovim is installed and accessible:

bash

neovim --version

This command should display the Neovim version, confirming that the installation was successful.
Notes

    By installing Neovim locally in ~/neovim, you do not need system-wide permissions.

    This method allows you to have a separate Neovim installation specifically for your user while keeping the system-wide installation untouched.

    You can update Neovim later by pulling the latest changes from the repository:

    bash

    cd ~/neovim
    git pull
    make -j4
    make install

    If you encounter any issues during the build process, they are likely due to missing dependencies or system-specific configurations. You may need to install additional development libraries or consult the Neovim documentation for troubleshooting.

This process should install the latest version of Neovim locally without requiring system-wide permissions.








git clone --depth 1 https://github.com/AstroNvim/AstroNvim ~/.config/nvim


