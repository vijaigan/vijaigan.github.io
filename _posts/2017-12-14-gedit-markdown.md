---
title: "gedit markdown install notes "
categories:
  - Linux
tags:
  - gedit
  - markdown 
  - Linux 
last_modified_at: 2019-03-28
--- 

# gedit markdown install 

## [gedit markdown home page](https://github.com/jpfleury/gedit-markdown) 

1. gedit markdown depends on - python3-markdown 
2.  wget https://github.com/jpfleury/gedit-markdown/archive/master.zip
3.   unzip master,zip 
4.   as non-root user run gedit-markdown.sh install 


~~~~
root@raghar:~# apt-get install python3-markdown
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  python3-pygments python3-yaml
Suggested packages:
  python-markdown-doc ttf-bitstream-vera
The following NEW packages will be installed:
  python3-markdown python3-pygments python3-yaml
0 upgraded, 3 newly installed, 0 to remove and 96 not upgraded.
Need to get 753 kB of archives.
After this operation, 3,934 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://deb.debian.org/debian stretch/main amd64 python3-markdown all 2.6.8-1 [56.6 kB]
Get:2 http://deb.debian.org/debian stretch/main amd64 python3-pygments all 2.2.0+dfsg-1 [588 kB]
Get:3 http://deb.debian.org/debian stretch/main amd64 python3-yaml amd64 3.12-1 [108 kB]
Fetched 753 kB in 1s (408 kB/s)       
Selecting previously unselected package python3-markdown.
(Reading database ... 217970 files and directories currently installed.)
Preparing to unpack .../python3-markdown_2.6.8-1_all.deb ...
Unpacking python3-markdown (2.6.8-1) ...
Selecting previously unselected package python3-pygments.
Preparing to unpack .../python3-pygments_2.2.0+dfsg-1_all.deb ...
Unpacking python3-pygments (2.2.0+dfsg-1) ...
Selecting previously unselected package python3-yaml.
Preparing to unpack .../python3-yaml_3.12-1_amd64.deb ...
Unpacking python3-yaml (3.12-1) ...
Setting up python3-yaml (3.12-1) ...
Setting up python3-markdown (2.6.8-1) ...
Setting up python3-pygments (2.2.0+dfsg-1) ...

gvijai@raghar:~/gedit-markdown/gedit-markdown-master$ ./gedit-markdown.sh install 
############################################################
##
## Installation of gedit-markdown
##
############################################################

mkdir: created directory '/home/gvijai/.local/share/gtksourceview-3.0'
mkdir: created directory '/home/gvijai/.local/share/gtksourceview-3.0/language-specs'
mkdir: created directory '/home/gvijai/.local/share/gedit'
mkdir: created directory '/home/gvijai/.local/share/gedit/plugins'
mkdir: created directory '/home/gvijai/.config/gedit/snippets'
mkdir: created directory '/home/gvijai/.local/share/gtksourceview-3.0/styles'
'config/gedit-markdown.ini' -> '/home/gvijai/.config/gedit/gedit-markdown.ini'
'language-specs/markdown-extra.lang' -> '/home/gvijai/.local/share/gtksourceview-3.0/language-specs/markdown-extra.lang'
'snippets/markdown-extra.xml' -> '/home/gvijai/.config/gedit/snippets/markdown-extra.xml'
mkdir: created directory '/home/gvijai/.config/gedit/tools'
'tools/export-to-html' -> '/home/gvijai/.config/gedit/tools/export-to-html'
'plugins/markdown-preview/markdown-preview' -> '/home/gvijai/.local/share/gedit/plugins/markdown-preview'
'plugins/markdown-preview/markdown-preview/__init__.py' -> '/home/gvijai/.local/share/gedit/plugins/markdown-preview/__init__.py'
'plugins/markdown-preview/markdown-preview/locale' -> '/home/gvijai/.local/share/gedit/plugins/markdown-preview/locale'
'plugins/markdown-preview/markdown-preview/locale/fr' -> '/home/gvijai/.local/share/gedit/plugins/markdown-preview/locale/fr'
'plugins/markdown-preview/markdown-preview/locale/fr/LC_MESSAGES' -> '/home/gvijai/.local/share/gedit/plugins/markdown-preview/locale/fr/LC_MESSAGES'
'plugins/markdown-preview/markdown-preview/locale/fr/LC_MESSAGES/markdown-preview.mo' -> '/home/gvijai/.local/share/gedit/plugins/markdown-preview/locale/fr/LC_MESSAGES/markdown-preview.mo'
'plugins/markdown-preview/markdown-preview/locale/fr/LC_MESSAGES/markdown-preview.po' -> '/home/gvijai/.local/share/gedit/plugins/markdown-preview/locale/fr/LC_MESSAGES/markdown-preview.po'
'plugins/markdown-preview/markdown-preview/locale/markdown-preview.pot' -> '/home/gvijai/.local/share/gedit/plugins/markdown-preview/locale/markdown-preview.pot'
'plugins/markdown-preview/markdown-preview.plugin' -> '/home/gvijai/.local/share/gedit/plugins/markdown-preview.plugin'
removed '/home/gvijai/.local/share/gedit/plugins/markdown-preview/locale/markdown-preview.pot'
removed '/home/gvijai/.local/share/gedit/plugins/markdown-preview/locale/fr/LC_MESSAGES/markdown-preview.po'
'styles/classic-markdown.xml' -> '/home/gvijai/.local/share/gtksourceview-3.0/styles/classic-markdown.xml'

Installation successful. Please restart gedit (if it's already running).

~~~~ 
