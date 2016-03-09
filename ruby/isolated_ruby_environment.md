# isolated ruby environments

To my knowledge there exist to widely used tools to accomplish the task.
There is [rbenv](http://rbenv.org/) and [rvm](https://rvm.io/‎).
I choose rbenv because to me it seems more lightweight and easier to understand. 

```bash
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
cd ~/.rbenv && src/configure && make -C src
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.profile
~/.rbenv/bin/rbenv init
```

logout / login

```bash
rbenv install -l
rbenv install 2.2.3
mkdir  ~/ruby_project && cd ~/ruby_project
rbenv local 2.2.3
gem install bundler
```