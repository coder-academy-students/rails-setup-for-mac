<p align="center"><img src="https://github.com/coder-factory-academy/cf-guidline-css/blob/master/CFA.png"></p>

# Install Rails on Mac

Hopefully you have a recent version of Mac OSX installed.

01. If you have Mavericks (10.9) or Yosemite (10.10), you can install Command Line Tools using this command. Choose to install and follow the prompts.

  In your terminal, type `xcode-select --install`

02. If you have an earlier version of OSX, you will probably need to install Command Line Tools by downloading it from the Apple Developer Downloads site.

  Once you're registered and signed in, you can search for Command Line Tools and download/install the latest version for your OSX version.

03. Check that Command Line Tools have installed

  In your terminal, type `gcc --version`

  You should see a similar output to this:
    ```
      Configured with: --prefix=/Applications/Xcode.app/Contents/Developer/usr --with-gxx-include-dir=/usr/include/c++/4.2.1
      Apple LLVM version 8.0.0 (clang-800.0.42.1)
      Target: x86_64-apple-darwin16.4.0
      Thread model: posix
      InstalledDir: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin
    ```

04. Install HomeBrew
    ```
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

05. When that finishes, run `brew doctor`

06. *rbenv* can manage all your versions of ruby - rbenv is also available on linux and windows with Bash which keeps things familiar to you. Use HomeBrew to install rbenv:
  ```
    brew install rbenv
  ```

07. Add some code to your .bash_profile file. In the terminal:
  ```
    echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
    echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
  ```

09. Close and then reopen your terminal.

10. Install Ruby 2.4.0 and set it the working version.
  ```
    rbenv install 2.4.0 && rbenv local 2.4.0
  ```

11. Install Rails 5
  ```
    gem install rails --version 5.0.1 --no-ri --no-rdoc && rbenv rehash
  ```

12. In the terminal enter ```rails -v``` to confirm it is installed


You're done!
