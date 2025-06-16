```bash
xcode-select --install
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install ruby
```


```bash
echo 'export PATH="/opt/homebrew/bin:$PATH"' >> ~/.zshrc
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
echo 'export PATH="/opt/homebrew/lib/ruby/gems/3.6.9/bin:$PATH"' >> ~/.zshrc # pay attention to version
source ~/.zshrc
```


```bash
gem install bundler
bundle install
```

```bash
bundle add csv
bundle add logger

bundle exec jekyll server
```