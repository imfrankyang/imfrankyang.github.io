# LaTeX installation


## install on ubuntu Texlive

https://www.tug.org/texlive/  

**method 1**

```
sudo apt install texlive-latex-extra
sudo apt install texlive-full
```

texlive-base - 160 MB
texlive-latex-recommended - 203 MB
texlive - 269 MB
texlive-latex-extra - 464 MB
texlive-full - 5903 MB

**method 2** full iso

download iso file from https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/Images/  

uninstall first
```bash
sudo apt purge texlive*
sudo rm -rf /usr/local/texlive/*
rm -rf ~/.texlive*
sudo rm -rf /usr/local/share/texmf
sudo rm -rf /var/lib/texmf
sudo rm -rf /etc/texmf
sudo apt remove tex-common --purge
find -L /usr/local/bin/ -lname /usr/local/texlive/*/bin/* | sudo xargs rm
```
install
```bash
sudo apt-get install perl-tk perl-doc

sudo mount -o loop texlive.iso /mnt
cd /mnt 
sudo ./install-tl

#env .bashrc
export PATH=$PATH:/usr/local/texlive/2020/bin/x86_64-linux
export MANPATH=/usr/local/texlive/2020/texmf-dist/doc/man
export INFOPATH=/usr/local/texlive/2020/texmf-dist/doc/info
```

**method 3**

download `install-tl-unx.tar.gz` from https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/tlnet/

```bash
wget https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/tlnet/install-tl-unx.tar.gz
tar -xzf install-tl-unx.tar.gz

sudo ./install-tl -repository https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/tlnet/
sudo ./install-tl -gui -repository https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/tlnet/
sudo apt-get install perl-tk perl-doc

```

update Texlive

https://www.tug.org/texlive/tlmgr.html

```bash
sudo tlmgr option repository https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/tlnet
tlmgr repository set http://mirror.hust.edu.cn/CTAN/systems/texlive/tlnet	#华中科技大学的镜像

tlmgr update --self
tlmgr update --all
tlmgr update --list	#列出需要更新的包
```

test

```bash
vi hello.tex
\documentclass[UTF8]{ctexart}
\begin{document}
欢迎来到 \TeX{} 世界！
\end{document}

xelatex hello
lualatex hello

xelatex -v	#test if succeed
```



{{< admonition tip ""  true >}}
sudo does not find tlmgr

```bash
sudo visudo
修改secure_path
Defaults        secure_path="/usr/local/texlive/2020/bin/x86_64-linux:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin"

```

{{< /admonition >}}



{{< admonition tip ""  true >}}

要在整个系统中使用 TEX 字体，还需要将 TEX 自带的配置文件复制到系统目录下

```bash
sudo cp /usr/local/texlive/2020/texmf-var/fonts/conf/texlive-fontconfig.conf /etc/fonts/conf.d/09-texlive.conf
sudo fc-cache -fv	#刷新字体数据库
```

{{< /admonition >}}



## install on Mac

UNIX 安装同ubuntu
env

```
echo "export MANPATH=${MANPATH}:/usr/local/texlive/2020/texmf-dist/doc/man" >> ~/.bashrc
echo "export INFOPATH=${INFOPATH}:/usr/local/texlive/2020/texmf-dist/doc/info" >> ~/.bashrc
echo "export PATH=${PATH}:/usr/local/texlive/2020/bin/x86_64-darwin" >> ~/.bashrc
```




## reference

* [Windows + Ubuntu 安装配置更新卸载 TeXLive 指南](https://matnoble.me/tech/ubuntu/install-texlive/#%E5%AE%89%E8%A3%85)
* https://www.tug.org/texlive/quickinstall.html
* https://www.tug.org/texlive/doc/install-tl.html
* https://www.bilibili.com/video/BV1tg4y1B7f3?t=1016

