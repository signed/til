# Adjust prompt

To display the branch name in the current working directory first fetch the [git prompt][git-prompt] script from git contrib and store it locally. Make sure it gets sourced by adjusting your ~/.profile accordingly.

````
FILE=~/bin/local/git-prompt.sh; mkdir -p ~/bin/local && \
curl --silent -o ${FILE} https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh && \
chmod +x ${FILE} &&\
echo . ${FILE} >> ~/.profile
````

Update the `PS1` environment variable to display what you want to see in the [prompt][documentation].

````
echo $'export PS1=\'\w$(__git_ps1\\n\'' >> ~/.profile
````


[git-prompt]: https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh
[documentation]: https://www.gnu.org/software/bash/manual/html_node/Controlling-the-Prompt.html#Controlling-the-Prompt
