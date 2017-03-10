FROM centos:7
MAINTAINER Richard<nibocn@gmail.com>

RUN yum makecache fast \
    && yum install -y git \
    && yum install -y zsh \
    && yum install -y vim \
    && git clone --depth 1 https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh \
    && cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc \
    && echo "bindkey '^R' history-incremental-pattern-search-backward" >> ~/.zshrc \
    && chsh -s /bin/zsh \
    && yum clean all

COPY vimrc /etc/

CMD ["/bin/zsh"]
